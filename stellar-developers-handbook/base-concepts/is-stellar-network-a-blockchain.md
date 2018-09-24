## Is Stellar Network a blockchain?

Stellar is an immutable distributed ledger. However, it's architecture is completely distinctive from, let's say, Bitcoin or Ethereum. There is no mining, no PoW or PoS algorithms, it resembles rather a database with a simplified API than Bitcoin sequence of blocks.
Like a traditional ledger, the Stellar ledger records a list of all the balances and transactions belonging to every single account on the network. A copy of the global Stellar ledger is hosted on each Stellar node.

These servers form a decentralized Stellar network, allowing the ledger to be distributed as widely as possible.
The Stellar servers communicate and sync with each other (a mechanism known as **consensus**) to ensure that transactions are valid and get applied successfully to the global ledger.

Immutability is one of the key blockchain concepts. All ledgers are sequential, and each new ledger is bound to its predecessor. 
A ledger represents the state of the Stellar universe at a given point in time. It contains the list of all the accounts and balances, all the orders in the distributed exchange, and any other data that persists.
Nobody can modify a block somewhere in the middle of the chain and enjoy one more million on the account balance because the whole chain becomes invalid. 
So we can safely assume that data on the blockchain is legitimate, having been verified by multiple network validators.

#### References

1. [Basics explainers from Stellar.org](https://www.stellar.org/how-it-works/stellar-basics/explainers/).
2. [Stellar Guides - Ledger](https://www.stellar.org/developers/guides/concepts/ledger.html).
3. [Stellar StackExchange - Is Stellar platform a blockchain?](https://stellar.stackexchange.com/q/1584/365).
4. [Table of Contents](../index)