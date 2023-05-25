## Blockchain
-------------------------------------
A *Decentralized* and *Distributed* system where all parties can view the entire records or transactions done.  

This means that no one party holds all the data and since all parties involved has complete copy of the trasnacations performed thereby preventing courruption.  

Also know as a Distributed Ledger since it stores a ledge of transactions.  

It is *Immumutable* meaning it can be updated with new transactions but cannot edit/modify previous data.  

Core techonologies involved [Cryptography, Encryption](), [Merkle trees]()
and [Wallets]() 

Transactions are performed on the basis of the public key corresponding to the private key using wallets.

The transactions are grouped togther and the *Miners* in the gather these bunch together and form them into a block using hashing and then grouped into chains using [Merkle trees]()

*Miners* take these blocks which contains Hash of Previous block, Transactions and Nonce value to generate a new Hash for that block.  

The Miner does the calculation to find the *Nonce* value to find the hash for the block according to the Blockchain network. 

If two blocks are mined simultaneously a fork is created then it is validated by longest Chain and any transactions in the shorter chain are not encorporated into the chain and it might be mined afterwards and incoporated to other chain.

[Reference Video](https://www.youtube.com/watch?v=qcuc3rgwZAE)
