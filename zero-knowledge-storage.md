# **Zero-Knowledge storage**

Iryo.network is a global repository of openEHR data. Since almost nobody wants to give medical data to “GoogleEHR” type of capture and shameless reaping of all the medical data for commercial purposes, Iryo decided to give up the access to plain data. Iryo perceives medical data it holds as a [“toxic asset”](https://www.schneier.com/blog/archives/2016/03/data_is_a_toxic.html), meaning that holding too much data in one place presents too big of a liability risk. What solves it is a Zero-Knowledge data storage which is resistant to all attacks, including state-actor or an inside job. It works by the user encrypting all his data on his device with his public key. His private decryption key stays on his device. Whenever someone wants to access patients data \(doctor, researcher…\) the patient has to approve the access \(by clicking yes in his IryoEHR app\),This gives a re-encryption key to doctor public key. You can read more under “Private key management section” to understand all the edge cases.

**    
**The same copy of encrypted health records is stored on the 3 geographically and managerially redundant storage nodes.

1.\) One encrypted backup copy stays on IRYO cloud node- by default, but it can be changed by a clinic or end user to point to another storage api. Iryo offering is centralized in the cloud with tight provisioning controls.  
Pros: audited, maintained, secured, backuped.  
Cons: centralized.

2.\) Second encrypted copy stays in your home clinic storage node.  
Pros: local copy, the clinic doesn't need to rely on the internet connection, fairly distributed.  
Cons: clinics IT personnel lack specialization on secure deployment.

3.\) End-user devices \(phones\) distributed all over the world.  
Pros: decentralized \(not centrally controlled\) protected by thousands of people at the same time  
Cons: not enough space for all raw data, malware infected devices, old devices, lost/stolen devices,...

Whenever data on End-user devices \(3\) gets updated, the device would connect to api of both redundant storage nodes \(1 and 2\) and sync/update encrypted data to match the local copy. Both storage nodes would provide a “blockchain proof” \(cryptographic receipt\) that they did actually save the data with the same hash clients wanted them to which clients would validate by asking independent node if the data was actually put in a chain.

![](https://lh4.googleusercontent.com/eQQqCqs6b7em5Rq80l-y7Esxivm3lV2In6jZL9idgMPJcBj3wbgw1YLG-LfgkQQZD9zDSMuIc-cnZeXc5i3aPV6zIG8ViT3SdEzD8SlPfK94ty0GH1a02uDjmVPVt6yHcOPawLIn)

If there is newer data that the device poseses \(for instance, doctor syncing your health record to most recent version\), then it would only connect to one endpoint api- one that is reachable, preferably the local one \(2\) in the same clinic. This way read access doesn’t consume hospital internet connection.

The diversity of network topologies and endpoint reachability would also let clinics operate even if their local network is down \(as long as they can find emergency hotspot\). This greatly reduces risks of \(possibly deadly\) access outages.

There could be a catastrophic data loss at each of these factors individually, but together they offer one of the strongest redundancies you would see in any system.

### **Risks in distributed data storage systems such as filecoin/sia/storj/maidsafe**

The problem with distributed systems like filecoin/sia/storj/maidsafe is that they can’t protect you from attacker storing and serving all of the data from the single server. They can pretend to be geographically distributed and collect the money for all 3-5 copies \(Sybil attack\). Trusting your device, your hospital, and IRYO network to keep at least one \(encrypted\) copy alive offers far greater guarantees against health data loss.

### **Who pays for the storage in Iryo network?**

All text-based data will be covered by clinic staking the Iryo tokens, and the 1% yearly inflation on top of it would be partially used to cover the cost of Iryo storage.

For the possibility of gigabytes of other raw data, the clinics would have to stake more. If users find themselves at the mercy of their clinic, they would have the option to stake coins themselves. That would unlock the storage for them, and limit the abusers.

The exact staking requirement would be updated based on the real data we gather when the Iryo network goes live. We strongly suggest that it would be cheaper than any decentralized storage at scale, especially way cheaper than proprietary systems that cannot be easily upgraded.

Iryo network refuses to be part of risky “Big Data” obsession and rather focus on patient privacy. That would allow Iryo network to scale globally, allowing it to attract more users. The fact that users/clinics/governments can feel safe storing data on Iryo platform means that addressable pool of users willing to share their data with researchers would also grow larger than ever before.

Open-source end-user apps would ensure that there are no secret back-doors circumventing the protection.

Since health data doesn’t decrypt itself without patient consent, the whole new approach needs to be devised to allow for machine learning- ‘Artificial Intelligence’ capabilities;

