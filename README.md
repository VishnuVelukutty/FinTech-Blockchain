## Index
-------------------------------------------------------------------
### 1. [Blockchain](#blockchain)
- Working

### 2. [Cryptography-Encryption](#cryptography-encryption)
- Public key
- Hashing Algorithm
- Encoding

### 3. [Wallets](#wallets)
- Working
- Types

### 4. [Bitcon](#bitcon)
- Working
- Turing Complete
- Proof of Work (PoW)
- Double Spending
- Merkle Tree
- UTXO 
- DLT

### 5. [Etherum](#etherum)
- Proof of Stake (PoS)
- PoW v/s PoS


___________________________________________________________________

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

*Miners* take these blocks which contains Hash of Previous block, Transactions in the block and Nonce value to generate a new Hash for that block.  

The Miner does the calculation to find the *Nonce* value to find the hash for the block according to attributes set by the Blockchain network (e.g a hash starting with 4 zeroes).This is also reffered to as Proof of work/Mining.On successful calculation they recieve rewards for it.  

If two blocks are mined simultaneously a fork is created then it is validated by *Longest Chain* and any transactions in the shorter chain are not encorporated into the chain and it might be mined afterwards and incoporated to other chain.

[Reference Video 1](https://www.youtube.com/watch?v=qcuc3rgwZAE)  
[Reference Video 2](https://www.youtube.com/watch?v=bBC-nXj3Ng4)   
[Reference Video 3](https://www.youtube.com/watch?v=2yJqjTiwpxM)   
[Reference Video 4](https://www.youtube.com/watch?v=aQWflNQuP_o) 


[Back](#index)
___________________________________________________________________

## Cryptography-Encryption
___________________________________________________________________

Cryptography is the science of concealing messages with a secret code. 

Encryption is the way to encrypt and decrypt data. 

The first is about studying methods to keep a message secret between two parties (like symmetric and asymmetric keys), and the second is about the process itself.


- *PUBLIC KEY*  

    Uses one key for encryption and another for decryption; also called asymmetric encryption. Primarily used for authentication, non-repudiation, and key exchange.  

    1. ECC
    2. ECSDA
    3. BIP 32 & 39 (Based on ECC)

- *HASHING ALGORITHMS*  

    Uses a mathematical transformation to irreversibly "encrypt" information, providing a digital fingerprint. Primarily used for message integrity. A signature that aids in sending any file that confirms that the file has arrived the destination is intact without any courruptions or tampering (a check digit like a barcode or credit card) for the entire file which basically a hexa-decimal or 16, 32, 64 bits in size (a long number that sums everthing in that file/summary).  
    
    Has 3 main requirements 
    1. Should be reasonably fast but not too fast since it can be cracked. 
    2. If one bit is changed anywhere in the file the whole hash should be completely different (avalanche effect).
    3. Hash collisions must be avoided (2 documents cannot have the same hash).

    1. SHA-256
    2. KECCAK
    3. RIPEMD

- *ENCODING*  

    The way in which symbols are mapped onto bytes, e.g. in the rendering of a particular font, or in the mapping from keyboard input into visual text.

    1. RLP 
    2. 

[Overview Reference](https://www.garykessler.net/library/crypto.html#skc)
[]()  
[Back](#index)

___________________________________________________________________
## [Wallets](https://www.youtube.com/watch?v=AQO7KePXUEQ)  
___________________________________________________________________

Used for creating and storing for the public and private keys of an user, interacting with blockchain since the cryptocurrencies are basically linked to the user's private key, monitors balances and enables to send or recieve cryptocurrencies.  


Types :
1. [HD Wallets](https://www.youtube.com/watch?v=A1Pl5hYHXiI)
Hierarchical deterministic (HD) wallets generate a seed or mnemonic phrase which is string of common phrase to regenate the private keys. The same seed and can be used to create multiple unique addresses.

1. Hot Wallet  
Creates and store private keys online e.g. Desktop and Mobile wallets which are connected to internet (HOT). Less secure since it is always connected to the internet.

2. Cold Wallet  
Creates and store private keys offline also know as Hardware wallet and needs to connected in order to perform transactions.
More secure since the hardware device can be disconnected from  the internet.




[Back](#index)


___________________________________________________________________
## Bitcon
___________________________________________________________________
- Working  

    Based on the principles of the blockchain. When a transaction is done it is signed by the sender using wallets and miners work on it to find the hash. 

    Bitcoins are fixed in count in order to prevent inflation. The total cap is of 21 million and around 19 million bitcoins have been mined (as of 2023) and are in circulation, leaving approximately 2 million left to be mined. Estimated that all bitcoins will be mined by the year 2140. Once this happens miners will no longer recieve mining rewards only transaction processing fees will be availed.   

    Halving events : Block Rewards  
    
    2012 : 25 BTC   
    2016 : 12.5 BTC  
    2020 : 6.25 BTC  
    2024 : 3.125 BTC  

- [Turing Complete](https://www.bitstamp.net/learn/blockchain/what-is-turing-complete/)  

    Turing Complete refers to a machine that, given enough time and memory along with the necessary instructions, can solve any computational problem, no matter how complex. The term is normally used to describe modern programming languages as most of them are Turing Complete.

- [Proof of Work](https://www.youtube.com/watch?v=3EUAcxhuoU4)
    Used as a consensus algorithm to validate and add new blocks. Miners competes for finiding the solution and if the miner finds the solution(i.e block hash with certain conditions) it is then verified by other Miners for authenticity.

- Double Spending  

    Refers to use of the same coin used to pay for different entities. Validations are performed in order to check if the transaction is possible. If both transactions are validated simultaneously then a fork is created and *Longest Chain* is preffered (*Six-confirmation wait* since it's unlikely to happen for more than six times aka Consenus Mechanism). 

- [Merkle Tree](https://www.youtube.com/watch?v=n6nEPaE7KZ8) 

    A DSA used to for organizing data that is made up of hash number of various data blocks of trasanctions performed in the blockchain network acts as a summary of all the transactions.
    The array size is 2<sup>n</sup> for e.g an array of size 4
    will be represented in the following way :

             H1234
            /    \ 
          H12     H34
          / \     / \
        H1  H2  H3  H4

    where H1234 is root hash. If the array size is not 2<sup>n</sup> then the last element is duplicated and compute its hash.  

                  H1234565'6'
                  /        \
             H1234         H565'6'
            /    \        /    \
          H12     H34   H56    H5'6'
          / \     / \    / \    / \
        H1  H2  H3  H4  H5 H6  H5' H6'
 




- [UTXO](https://www.youtube.com/watch?v=0_5wb5agLqE) 
    Unspent Transaction Output defined as the amount of bitcoin assigned to any address.
    For e.g In a Bank when you deposit some amount like a *5 x 100 rupee notes*, the bank will register it in their system and when you withdraw *500 rs.* the exact same *note* will not be given to you or it maybe a combination of 100+200+200 or a single 500 rs note.
    This in contrast to personal piggy bank when you accumulate
    the same amount *5 x 100 rupee notes* when withdraw from it you will get the same *5 x 100 rupee notes*.
    This is how things work in cryptocurrency, the wallet always shows the aggregate of all the transaction amount but under the hood it is UTXO i.e a single 0.9 BTC is not fundamentally equal to 0.1 BTC sent 9 times.



- [DLT vs Bitcoin](https://www.youtube.com/watch?v=JjMWrXqsrUs)  

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
        - an open permissioned blockchain as it shares data only with the parties involved in the transaction i.e need to know basis (blockchain transmits to all nodes) 

  





[Back](#index)



## Etherum

- [Proof of Stake](https://www.youtube.com/watch?v=YudpU58uYuM)
    Since Proof of Work requires all miners to run their computation all time in order to earn rewards this increases power consumptions, Proof of Stake on the other hand requires less work and energy since this method involves a lottery (pusedo-random election process) system wherein the  miner is randomly selected by the blockchain and then that miner performs the validation and recieves rewards.

    In order to ensure that no malicious activity takes place the miner has to *Stake* a certain amount of its cryptocurrency as a security. If the miner performs a malicious activity then the miner is penalized and certain reward is given to the spotter. 

    To improve the chances of being a miner one can stake more coins. The miner can also be selected on the basis of reputations or age.  

    This method only pays transaction fees.

-[EVM](https://www.quicknode.com/guides/ethereum-development/getting-started/what-is-the-ethereum-virtual-machine-evm/)
The Ethereum Virtual Machine (EVM) is the computation engine for Ethereum that manages the state of the blockchain and enables smart contract functionality. The EVM is contained within the client software.

In transaction execution, the EVM executes tasks (e.g., function calls to a smart contract) by interpreting the instructions in Opcodes (machine instructions at a low level); however, the data is formatted in bytecode. To get the data into bytecode, you can use a programming language such as Solidity (i.e., the native programming language for smart contracts) to compile and deploy the smart contract using bytecode. 

i.e Solidity code -> Byte code -> Opcode 

- [Nodes]()

 
[Back](#index)
