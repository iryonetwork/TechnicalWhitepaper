# **Private Key Management**

**  
**Private keys are long, random, and should never leave the end-user machine. Even if the encrypted data is leaked to the public it is still useless without the private key. They are about decentralized control of the encrypted data and value.  
  
But if you lose your keys, you lose everything that was encrypted with it. All your data, credentials or value. This is why encrypted services provide nerve-wrecking experience for most people. Some services are trying to solve this problem with recovery codes, which should be printed out and put into a safe drawer. It is safe to say that there is no mobile printer on your phones, and there is no mobile safe drawer. Most people don't have "safe drawers", not even in their homes. In reality, this approach works as an excuse, that services use to shift the blame to the user, thus avoiding legal and reputational liability.  
  
This is why most projects try to “solve” this problem by re-introducing centralized solutions for key recovery. Iryo network is taking a different, more distributed route.  


In the Iryo network private keys are everywhere. If we group them:  
  
**Patient keys**:  
**PK-1**Master private key derives 2 keys \(using BIP32\), that are used for;  
• medical data encryption key in the IryoEHR app  
• EOS ‘emergency access controls’ and wallet private key in the IryoEHR app

  
**Doctor keys**:  
**DK-1 **Master private key derives 2 keys \(using BIP32\), that are used for:  
• medical data encryption key in the IryoEHR app   
• EOS ‘access controls’ and wallet private key the IryoEHR app

  
**Clinic keys:**  
**CK-1 **half of the emergency medical data re-encryption key. One for each patient  
**CK-2** EOS ‘emergency access controls’ and wallet private key  
**CK-3** \(optional\) cloud backup AES encryption key; clinic can encrypt and then backup all their data to iryo.network



**Iryo keys**:  
**IK-1 **EOS attestation key  
**IK-2**Iryo EOS \(account funding\) wallet private key

  


**Token holder keys**:  
**TK-1 **EOS wallet private key for EOS wallet app.



### What happens if a user loses the device?

\(assuming he doesn’t have a second device with the same key\)  
  
For **PK-1 **\(patient medical data encryption key\), the simplest answer is that patient visits his/her doctor, that can use his device to issue a re-encryption key back to patients new device; together with signed permission message, that would replace patients wallet private key with a new one. If a patient doesn’t want to visit his doctor every time his/her device gets destroyed, he/she can save \(and move\) the key to the ZeroPass app \(see below\), using one-click magnet link. When keys are protected with ZeroPass, a patient can revoke the ability of his doctor to re-assign his key, leaving the patient in full control.  
  
If the patient’s personal doctor does access recovery instead of recovering master key via ZeroPass the patient’s wallet would get emptied, because the doctor can’t recover the actual keys but can only give access to patients new key. Using ZeroPass solves this problem. Whenever patient receives an Iryo token he will be asked to secure them within ZeroPass web of trust.



For **PK-1**,**TK-1 **the ZeroPass distributed and trustless recovery service can be used. In practice, patients would just click on magnet link inside the IryoEHR app, that would save \(and move\) all his/her keys; **PK-1 **and **DK-1** from IryoEHR to the ZeroPass app, automatically.



For Clinic and Iryo keys \(**CK-1**,**2**,**3 **& **IK-1**,**2**,**3**\), the ZeroPass 4Teams would be used.

  


