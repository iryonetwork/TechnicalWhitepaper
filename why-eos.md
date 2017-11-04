# **Why EOS?**

### Choosing the right platform, EOS overview. 

  
In general, there are two extremes in public blockchain tech:  
• using Proof of Work chain offers immutability and censorship resistance, but you pay for that with fees for every transaction.  
• using federation/dpos/masternodes offers speed and low fees/cost.  
  
Most tokens on these platforms have a centralized team behind them, which means that if their token contract is compromised, they should be able to roll it back \(or they can just issue a new contract with pre-hack balances etc\).  
  
Having a token that is solidified with PoW brings additional liability if something goes wrong. This is not a feature startup raising money should go for, at least not until their code is not tested by time.  
  
Ethereum sits in a thankless middle. It does not allow rolling back your app, since you don't really control your smart contract. Futhermore, you still need to compete for a limited blockspace and bid with gas or often just wait your turn \(could be a day\). For many token issuers that is just not needed.  
  
Token issuer requires just enough decentralization that the market perceived it as decentralized and it's history to be independently verifiable \(many/enough nodes that check it\). Of course, they also need tokens to be easily listed on the exchanges - once the platform is added, there shouldn't be too much work adding additional tokens.  
  
EOS will offer "shards" \(they call it blockchain apps\), which you would be able to use on your partitioned network - your nodes can discard all other messages, making them as light as your chain is designed to be. Lightly designed blockchain app would have the ability to spread more nodes since it's easy enough to verify, even if the whole EOS network gets "bloated".  
  
Instead of transaction fees EOS chooses a smarter way to charge. Every blockchain app \(shard\) must deposit coins for their users \(1% of locked coins mean that users of this app can get 1% of all bandwidth of block producers\)... and until your app only uses 1% of the whole EOS ecosystem, all the transactions are free for end-users.  
  
That way new users don't need to pay anything... but "app" developer still has to mind the resources, or the requirement to buy more and more EOS tokens to stake would kill his "app".  
  
Block-producers dilute this stake with up to 5% per year inflation, to pay for investment in additional bandwidth, space or execution/verification CPU power.  
There is one potential problem here; whenever block-producers upgrade their equipment, the requirement for tokens your app requires falls. Because you don't need those EOS tokens people might sell them on an open market and crash the price. Because token holders vote for block-producers, they might start voting for those who don't want to upgrade, to keep the staking requirements high. It would be interesting to see how would the tension between helping app developers with adoption and high token price play out.  
  
EOS user accounts; application developers will need to pay for the cost of those. Let's hope the price for them won't skyrocket. Otherwise, creation of fake user accounts \(by competition\) might drain the funding of the app.



Another plus is a focus on WebAssembly instead of solidity \(C++ toolchain compatibility\).



In addition to that, we would use public EOS network to keep the access control time-stamped and synced on all nodes. We deemed the importance of access control messages and history logs to be propagated near-real time in emergency situations. This cannot be achieved/guaranteed on the network like Ethereum or Bitcoin.

**  
**

