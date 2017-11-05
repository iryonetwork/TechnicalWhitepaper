## **ZeroPass App**

ZeroPass is a passwordless keychain & private key recovery manager. It can store keys in a zero-knowledge manner and provides trustless recovery \(that works even if ZeroPass servers are down\). The App development iscurrently in the private beta stage.**    
**Read more in depth on it on [zeropass.io](https://www.zeropass.io/) or fairly [technical whitepaper](https://www.gitbook.com/book/zeropass/whitepaper/details);

To use a key from ZeroPass users don’t need to remember anything; instead they need to sign every request for a requested key with 2 devices; devices that have been previously paired with ZeroPass app or optionally “yubikey style” devices \(FIDO compliant\).

Later, ZeroPass would add multisig transaction signing \(threshold ecdsa\), which will be used to provide extremely secure signing using private key -it stays secure even if one of your devices is infected by malware.This capability will be tightly integrated into IryoEHR app - the token section. ![](https://lh6.googleusercontent.com/UXdlBaZePqH7p4TTqJ4v4JDgj4QONUhpoXv8f9_OWLeQDkcKLYZdw1HreLnXWwXIE0TxKEiAtCZJqDqOLW-RDxHcmZzxNLqskNBcFVdTkQGLu10G9rysNY2Fh0LCCV0U4z6NPxtw)

** **If you lose your devices \(ZeroPass “factors”\) and lock yourself out the two out of three trusted contacts can help you recover \(within the app, or offline in case the service is unavailable\).**        
**

## **ZeroPass 4Teams app**

ZeroPass 4Teams will \(when ready\) provide clinics /and iryo multi-member teams environment with all core ZeroPass functionalities and benefits, while at the same time also taking into consideration their specific requirements:

• global overview of all members and their actions,  
• access to signing using private key for multiple users \(sharing functionality\),  
• adjustable level of security \(how many users and/or devices per user are required to sign transaction, or get access to the key\).

The use of user own devices will be encouraged as primary and/or second factor. This is a ZeroPass answer to provide security in the rising ‘bring your own device trend \(BYOD\)’. Knowing that 50%+ of all employees use their own devices for work, the trend does not seem to be slowing down.

All described key \(and subsequently health data\) recovery procedures might go out the window in extreme situations, such as long internet outages,... which put lives in danger.

To avoid fall-outs we would put in place a couple of disaster access modes, that patients or the whole clinic, can opt-out from:

### **Edge case: Emergency access for individual users**

Unconscious patient rushed with ambulance in the middle of the night:

The previous assumptions about a patient or his personal doctor being able to unlock the data can prove fatal in those cases. The solution is to escrow \(split with Shamir secret\) the re-encryption key within the ZeroPass 4Teams app and lock it with the smart contract \(enforced by ZeroPass server\). The smart-contract rules state that if the clinic wants to access the \(missing half\) of the key for patient Alice \(identified just with her public key\), the clinic needs to put 1000$ worth of IRYO tokens \(adjustable by Alice\) to the 1-month contract with her EOS wallet public key.

Now Alice IryoEHR app shows her the notification; if her medical data access was unjustified she has 1 month time to claim the 1000$ worth of tokens. If it was a legit life-threatening situation she can either approve the refund to the clinic or wait a month for a contract to expire- which would return all the tokens automatically to the clinic.

To stake the coins for emergency request clinic takes the tokens it already has from their wallet \(10.000$ worth of IRYO tokens\) and has 1 month time to replenish the stake if it gets under ‘staking requirement’ for the clinic. This way they don’t need to hurry with trying to buy the token in an already stressful situation, it’s just a matter of enough people in the clinic to approve the access. If multiple devices of a clinic got hacked \(very low probability\),the clinic stake would be drained and the hack would stop after 10 unauthorized accesses \(because the clinic would run out of tokens\).

Instead of 1000+ stolen Electronic health records only up to max 10 records can be leaked in the catastrophic event of data breach.

Potential abuse of this edge case functionality

• If Alice \(patient\) abuses the stake; the clinic can invoice her and later file a lawsuit if the invoice was not paid for.  
• If Alice hospital was issuing fraudulent requests she gets automatically compensated and can sue based on that public blockchain proof of the breach even if the clinic refuses to notify her of that catastrophic breach to multiple clinic personnel devices.**      
**

### **Edge case: Disaster ‘Health Records’ access mode for clinic**

ZeroPass 4Teams recovery works the same way as non team version; two out of three trusted users can help recover stored keys in the team app. Those trusted users might not have the app themselves they need other team members to prevent \(offline\) abuse.

This mode proves to be especially effective in case natural or other disasters occur where connection to the internet could be cut off or clinic’s devices are destroyed. A two out of three ZeroPass 4Teams trusted contacts can meet offline with team members that have the app and recover every single stored key together.

These modes are not designed to be extra easy for the user experience because a higher level of coordination prevents hackers to abuse disaster access mode. Hopefully, disaster access mode for clinic would never be used.

High net individuals head of the states and other individuals that might be targeted by criminal or nation-state hacking activities \(for instance, during a war\) can opt-out from the recovery access modes from the start. Individual patients can opt-out as well, as long as they provide consent that they understand the risks and use ZeroPass private key recovery app to its full extent \(with added two out of three trusted contacts\). Opting out should be discouraged by the clinic on an individual level because these ‘fail-safe modes” can help save patient lives.

