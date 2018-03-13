# whitepaper

INETO White Paper 2018 v1.0 Draft

### Problem Statement

Bitcoin was the first solution of distributed database, Etherum was the first smart-contract platform that built on the same principles as Bitcoin. All other altcoins have similar features or even the same code-base therefore they are in the same (first) generation of the distributed databases. 

First generation has the folowing problems:
* scalability (single blockchain, unlimited blocks, no trash collectors)
* privacy (all transactions and states are public)
* non efficient consensus algorithms (PoW)
* use hard forks for bug-fixing
* no KYC and AML

All thouse problems lead to the limited TPS (Transactions Per Second), vertical scaling and unlimited hard forks

### Vision

### Privacy

Ineto platform privides advanced level of privacy by using single transaction in a block. Each transaction in Ineto mixes inputs and outputs of different accounts by using two-phase commit protocol. Each atomic transaction between sender and reciever has additional 3 fields that other platforms does not have:
* sender address encrypted with random salt by reciever's public key
* reciever's address encrypted with random salt by sender's public key
* MEMO

Therefore, it will make all transactions in Ineto platform private, instead of public. 

### Fees

Bitcoin fees are calculated per transaction between miner and sender on market basis. In reality every transaction that miner creates is supported by all nodes. So, in contrary to Bitcoin whereas market is between current miner and a sender, in reality there is a market between networks and a sender. Finally, sender selects network to transfer value with lesser fees.

For network perspective, size of transaction and execution costs are almost constant and does not depend on amount. So, basically price that sender pays for the transaction must not depend on amount, and probably can depend on sender itself.

The goal is to achieve in distributed network effect, whereas trustfully accounts would be able to achieve zero fees.

So, basically it creates requirement of keeping transaction history of account and their scoring. 

### Coins

Ineto platform is going to support both: coins and accounts.

Each coin is the combination of public and private keys. Public key could be hidden by hash (like in Bitcoin). User can redeem coin until it has balance by using private key signature.

Initial version of Coins will support ECDSA algothim. 

Public address of the coin is Base64 of the byte array of ECDSA public key with prefix 'I1' that indicates that this is ineto coin address with version 1.

### Coins collector

To avoid support of unused coins in the system Ineto platform has coin collectors. Coin collector could be any participant that believes that some particular coin has no owner. To collect coin collector have to provide the bet or collateral that usually equals or less the balance of coin. If collector wrong, then he lose his bet and owner of coin adds the bet amount to the coin. If collector is right and coin owner did not redeem bet in 1000 blocks, then transaction automatically completed in a profit to coin collector.

### Accounts

### Known accounts

### Scoring

### Tokens

### Payments

### Consensus algorithm

### Verification

### Sliding blockchain

### Sharding

### State Machines

### Conclusion

### References

[1] Satoshi Nakamoto. Bitcoin: A peer-to-peer electronic cash system. https://bitcoin.org/bitcoin.pdf.
2008.

