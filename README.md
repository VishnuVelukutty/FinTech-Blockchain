-------------------------------------------------------------------
## Index
-------------------------------------------------------------------
### 1. [Blockchain](#blockchain)
### 2. [Cryptography-Encryption](#cryptography-encryption)
### 3. [Wallets](#wallets)
### 4. [Bitcon](#bitcon)
### 5. [Etherum](#etherum)


-------------------------------------------------------------------

## Blockchain
___________________________________________________________________
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
___________________________________________________________________

## Cryptography-Encryption
___________________________________________________________________

Cryptography is the science of concealing messages with a secret code. 

Encryption is the way to encrypt and decrypt data. 

The first is about studying methods to keep a message secret between two parties (like symmetric and asymmetric keys), and the second is about the process itself.


- *PUBLIC KEY*  
Uses one key for encryption and another for decryption; also called asymmetric encryption. Primarily used for authentication, non-repudiation, and key exchange.  

1. ECC and ECSDA
2. BIP 32 & 39 (Based on ECC)
3. 

- *HASHING ALGORITHMS*  
Uses a mathematical transformation to irreversibly "encrypt" information, providing a digital fingerprint. Primarily used for message integrity. A signature that aids in sending any file that confirms that the file has arrived the destination is intact without any courruptions or tampering (a check digit like a barcode or credit card) for the entire file which basically a hexa-decimal or 16, 32, 64 bits in size (a long number that sums everthing in that file/summary).  
Has 3 main requirements 
- Should be reasonably fast but not too fast since it can be cracked. 
- If one bit is changed anywhere in the file the whole hash should be completely different (avalanche effect).
- Hash collisions must be avoided (2 documents cannot have the same hash).

1. SHA-256
2. KECCAK
3. RIPEMD

- *ENCODING*  
The way in which symbols are mapped onto bytes, e.g. in the rendering of a particular font, or in the mapping from keyboard input into visual text.

1. RLP 
2. 

[Overview Reference](https://www.garykessler.net/library/crypto.html#skc)
[]()
-------------------------------------------------------------------
## Bitcon
-------------------------------------------------------------------
- Working
Based on the principles of the blockchain. When a transaction is done it is signed by the sender using wallets and miners work on it to find the hash. 

Bitcoins are fixed in count in order to prevent inflation. The total cap is of 21 million and around 19 million bitcoins have been mined (as of 2023) and are in circulation, leaving approximately 2 million left to be mined. Estimated that all bitcoins will be mined by the year 2140

Halving events : Block Rewards
2012 : 25 BTC 
2016 : 12.5 BTC
2020 : 6.25 BTC
2024 : 3.125 BTC

- Merkle Tree
A DSA used to for organizing data that is made up of hash number of various data blocks of trasanctions performed in the blockchain network acts as a summary of all the transactions.   

- UTXO 


- DLT vs Bitcoin
DLT : Distributed ledger 
TPS : number of  transactions that a network is capable of processing each second 

Traditionally DLT networks works on consensus timestamping 
this ensures that all transactions on the network agree with each other node in the platform 
need to provide proof of work which require computations therby increases time in turn gives low TPS


1. DAG
- Using Directed acyclic graphs (uni-directional) 
- nodes decide what happens (same as blockchain)
- verifies only 2 previous trasactions due to stronger relation
- more validations happens as network volume builds up


2. HashGraph 
- this methods achieves transaction success solely on consensus no PoW
- achieved with gossip about gossip and virtual voting and this also doesn't require pow
- little time in initation and transactions 
- morethan 250,000 tops
- fairness 
- cancellation is reduced by putting them in future blocks 

3. Holochain  
- decentralization of web (client-server model)no blockage /scalable
- mix of blockchain, torrent(P2P), Github
- each node will run on a chain of its own (nodes are independent) like siacoin ?
- DHT store data using certain keys (data is saved in actual location distributed in various locations across the globe )
- interactions are distributed
- no miners 

4. Corda
- an open permissioned blockchain as it shares data only with the parties involved in the transaction (blockchain transmits to all nodes)

## Wallets
## Etherum