# **Cryptographic enforcement of permissions**

### **over data using Proxy re-encryption \(NuCypher\)**

Public key cryptography \(PKC\) also known as asymmetric cryptography uses key-pair of public-private keys to encrypt/decrypt data. This property gives the user ability to share public key outside of his control. PKC based on elliptic curve is mostly used for digital data signing but it can be also used for data encryption.

[ECIES encryption](https://en.wikipedia.org/wiki/Integrated_Encryption_Scheme) allows you to asymmetrically encrypt data with a public key and decrypt it using private key, instead of typical two way symmetric AES cipher using one key for encryption and decryption. This is done by creating ephemeral random key based on receiver’s public key. Data is then symmetrically encrypted using this ephemeral key. Key is then cryptographically encrypted so that only the owner of the private key corresponding to the public key can decrypt it. Encrypted data along with encrypted ephemeral key is sent to the receiver.

This means that patient can share his public key with anybody to give them write-only permission.

> **ECIES\(patient\_public, data\)**

To read the data, a [Umbral](https://github.com/nucypher/nucypher-kms/blob/master/nkms/crypto/api.py#L384) algorithm is used, which allows patient to issue re-encryption keys. These keys can take the data and re-encrypt them to doctor public key on the fly!

To create re-encryption key, patient\_private, doctor\_public keys are used.  
Re-encryption key is then used to re-encrypt the data \(encrypted ephemeral key\) from the patient to doctor public key.

![](https://lh6.googleusercontent.com/Io7hvj0S6aL00zdT6-9oDOgl5JtbcoE3FKolKGc07np93bnZIwxei3w6d4GyEK8pglk-CZu-z9FQFPkXFoU8yFtSTY8Zse6_B96qqHSG8AzFRbwiuQpa6IRXrWb87i6tE2CF_vbi)  
Iryo storage nodes can now hol d \(patient issued\) re-encryption key, and re-encrypt all patient data to doctor on the fly. This way we only need to keep one copy of the same data, because it gets transmuted on the server, but still keeping it zero-knowledge.



In reality, the ECIES encryption is very slow. This is why NuCypher uses hybrid encryption scheme. The data is first encrypted with temporary key using AES symmetric cipher and this key is then encrypted with sender's public key using ECIES. Re-encryption is then done only over encrypted temp key rather than whole data. Read more detailed explanation in their [whitepaper](https://cdn2.hubspot.net/hubfs/2807639/NuCypher%20KMS%20Technical%20White%20Paper.pdf); NuCypher is building a decentralized service, but since Iryo has more trusted topology it can get same \(or better\) security properties deploying the Re-encryption software within the 2 storage node each user gets data served from.

# **Public key derivation \(**[**BIP32**](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki)**\)**

For the sake of simplicity of the paper, we only mention one encryption key-pair. In reality, the keys are deterministically derived from master private key. Separate child keys are used for different access permission levels. Each public child key would get separate re-encryption key, and this way the patient would have mathematical control level of permissions each doctor/specialist would get. [Youbase's whitepaper](https://paper.youbase.io/content/structured-data.html#path-levels) provides a good example of that model. 

## **Key rotation**

When access is revoked, a patient would issue new re-encryption keys for all new data. For old data, NuCypher proxy re-encryption relays on the servers to not serve the revoked clients \(with data or re-encryption keys\). In our case, Iryo storage node and clinic storage node would simply throw the revoked re-encryption keys away and by doing this they protect the data even in the event when storage node gets hacked later, and all encrypted data leaked.

Because of bip32 and proxy re-encryption, key rotation process does not need any other device but patient’s to be online \(it's non-interactive\). It gets better in the doctor’s case, where key rotation does not bother any of his patients, he can re-issue all re-encryption keys to himself.

