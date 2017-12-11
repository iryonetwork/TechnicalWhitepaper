# **Private Key Management**

**    
**Private keys are long and random and should never leave the end-user’s device. Should encrypted data be leaked to the public, it would be useless without the private key. The value of private keys lie in the decentralized control of encrypted data and value.

However, if you lose your keys, you lose the data, credentials and value that it encrypted. It is for this reason that encrypted services provide a nerve-wrecking experience for most people. Some services are trying to solve this problem with recovery codes that should be printed out and put into a safe drawer. It is safe to say that there is no mobile printer on your phones, and there is no mobile safe drawer. Most people don't have "safe drawers", not even in their homes. In reality, this approach is not practical for the user and rather has a stronger role in providing the service provider with immunity against legal and reputational liability.

While many other projects re-introduce centralized solutions for key recovery, the Iryo Network takes a different, more distributed route.

In the Iryo Network private keys are everywhere. These keys can be grouped into patient keys, doctor keys, clinic keys, Iryo keys and token holder keys.



**Patient keys**:  
**PK-1**: A master private key that derives two keys \(using BIP32\) which are used for:

* medical data encryption keys in the IryoEHR app

* EOS ‘emergency access controls’ and wallet private keys in the IryoEHR app

**Doctor keys**:  
**DK-1**: A master private key that derives 2 keys \(using BIP32\), that are used for:

* medical data encryption keys in the IryoEHR app 

* EOS ‘access controls’ and wallet private keys in the IryoEHR app

**Clinic keys:**  
**CK-1**: Half of the emergency medical data re-encryption key. One for each patient.

**CK-2**: An EOS ‘emergency access controls’ and wallet private key.

**CK-3 **\(optional\): A cloud backup AES encryption key that allows clinics to encrypt and then backup all their data to Iryo Network.

**Iryo keys**:  
**IK-1: **An EOS attestation key.

**IK-2**: An Iryo EOS \(account funding\) wallet private key.

**Token holder keys**:  
**TK-1**:** **An EOS wallet private key for EOS wallet app.

### What happens if a user loses the device?

For **PK-1**, assuming that the patient doesn’t have a second device with the same key, \(patient medical data encryption key\), the simplest answer is that they can visit their doctor, who can use his device to issue a re-encryption key back to patients’ new device. Together with signed permission message, this would replace patient’s wallet private key with a new one. If a patient doesn’t want to visit his doctor every time their device gets destroyed, they can save \(and move\) the key to the ZeroPass app \(explained later in this paper\) using a one-click magnet link. When keys are protected with ZeroPass, a patient can revoke the ability of his doctor to re-assign his key, leaving the patient in full control.

If the patient’s personal doctor performs an ‘access recovery’ instead of recovering a master key via ZeroPass, the patient’s wallet would be emptied. This is because the doctor can’t recover the actual keys but can only give access to patient’s new key. Using ZeroPass solves this problem. Whenever a patient receives an IRYO token he will be asked to secure them within the ZeroPass web of trust.

For **PK-1** and **TK-1 **the ZeroPass’ distributed and trustless recovery service can be used. In practice, patients would simply click on the magnet link inside the IryoEHR app, that would save \(and move\) all his/her keys; **PK-1 **and **DK-1 **from IryoEHR to the ZeroPass app, automatically. 

For clinic and Iryo keys \(**CK-1**,**2**,**3 **& **IK-1**,**2**,**3**\) the ZeroPass 4Teams app would be used.

