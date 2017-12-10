# **\(public\) Blockchain**



Blockchain is a continuously growing list of records, called blocks, which are linked and secured using cryptographic algorithms. Each block contains typically a hash as a link to a previous block, a timestamp and transaction data. Full-nodes validate all the transactions, but they can’t settle the disagreements in which order they receive them. To prevent double-spending, the whole network needs to reach global consensus on the transaction order which it achieves using centralized parties or decentralized proof of work or proof of stake algorithm \(and their derivatives\).

It’s important to know that your local blockchain node won’t allow anything that is not “valid” \(pre-defined\), even if the consensus algorithm says otherwise.

Contrary to popular belief and aggressive marketing, blockchains are not a good solution for storing data. Each piece of information that you store in the blockchain sits in hundreds or more nodes \(100.000+ in case of the bitcoin\), making it very costly. This is why Iryo network doesn’t store data on blockchain but uses blockchain for transparency of transactions.

Some projects pretend to be using blockchain by using private chains, which are usually just re-branded databases. They use some elements of blockchain technology but miss the core idea of it, which is offering oversight over the validity of the data stored.

Public blockchains are mainly useful for two things; value transfer \(including initial creation and distribution of value coins\) and trustless timestamping of the messages.

