# **Blockchain permission controls**

End user can issue signed permission messages to the blockchain. This includes:

• sharing all electronic health records with your personal doctor \(with or without time limits\), •revocations of access to patients EHR,

• sharing of limited relevant parts of health records with a specialist \(with a time limit\). Inpatient medical records will also be partitioned with a separate set of access rules.

• issuing IOT device permission to write, but not to read the data,

• rotating your re-encryption key.



Use of the smart contracts for permission controls is optional \(there is no double spending problem\). Iryo would use it, because that way EOS node can compute the state the minute it received the ordered message, instead of waiting for the query to compute it \(the state gets pre-computed\).



**Permission controls** benefit from being in the blockchain in the following ways:

• Trustless timestamping. All Iryo full nodes - including consensus “block-producing” nodes - would validate all the messages. There can’t be any doubt what and when blockchain permission messages were issued.

• Immutable log of all messages. It’s not possible to deny that the valid access request was issued. That will reduce the possibility of litigation with dishonest parties claiming they never issued the access permissions.

• Once your message gets included in the blockchain, one part of the network can not withhold it from another. That way, you can always be sure you have all the revocations, assuming you are running Iryo full node \(which is still just a tiny subset of the whole EOS network\).



All the storage endpoints \(in the cloud and in the clinics\) would run their independent Iryo ledger full node. A smart contract would be used to prepare the local state. Direct query on the full node would return either true or false for each access request the Iryo \(storage\) network needs to process.

![](https://lh3.googleusercontent.com/xN2SM-g16Vi2ZWQuPcWauNcWFONQCSgWEBIQPdfOEUdrKPul4H2OzblZ5BiKoKxmb1RIyLGgPyYF_VgrTphxk7g65cv-nSnzwwzp2n-NhX_4MukvNbQltFdjS29hgnG3Pyc2tkbe)

  


