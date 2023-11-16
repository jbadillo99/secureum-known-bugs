# Lesson 1: Blockchain Basics

## Dapp (Decentralized Application)

Web1:

The permissionless open source web with static content.

Web2:

The permissioned web, with dynamic content. Where companies run your agreements on their servers.

Web3:

The permisionless web, with dynamic content. Where decentralized censorship resistant networks run your agreement and code. It generally is accompanied by the idea of user owned ecosystems, where the protocols you interact with you also own a portion of, instead of solely being the product.

## Smart Contracts

### Definition:

- Cannot be altered (immutable)
- Automatically executes
- Everyone sees the terms of the agreement

## Trust Minimized Agreements (Unbreakable Agreements)

1. Decentralized

- Node Operators can compute different versions of the blockchain

2. Transparency & Flexibility

- No shady deals, because everybody has the same rules

3. Speed & Efficiency

- Unlike clearing houses transactions are instant

4. Security & Immutability

- Hacking a blockchain is extremely difficult (need a private key)

5. Counter Party Risk Removal

- Cannot alter the terms of the deal

6. Trust minimized agreements

- Doing the right thing is infrastructural

## DeFi (Decentralized Finance)

- Financial products with the result of finance

## Faucets

A Faucet is used to provide tokens for the test net that is being used.
It provides tokens for the user to be able to send transactions which
are required for the to run smart contracts and send tokens between addresses.

### Chainlink faucet

**Note**

As of August 2023 the mostly used Ethereum Testnet is Sepolia

**Link**
[Link to Chainlink Faucet Here](https://faucets.chain.link/sepolia)

## Mining

Nodes try to find the Nonce for the given block number and data. The node
that solves the problem to compute the Nonce gets a reward for solving the problem.
This mining method is known as Proof of Work (PoW)

### Block

A block is a list of transactions mined together
To mine a valid block the block will need to mine the block number,new data, the previous block hash,
its valid Nonce. Anytime a hash is invalid the chain becomes invalid.
_This is why blockchains code is **immutable**_

#### Genesis Block

The genesis block is the first block in the block chain with no previous hash

### Nonce

A "number used once" to find the solution to the blockchain problem
Also used to define the transaction number for an account/address.

### Keys

Only known to the key holder, it's used to "sign" transactions.
Uses the ECDSA (Elliptic Curve Digital Signature Algorithm) to create a private and public key pair
This Algorithm provides an authentication method used where a public key pair and a digital certificate are used as a signature to
verify the identity of a recipient or sender of information.

#### Private Keys

Private keys are held only by the user and are used to digitally sign transactions by the user

#### Public Keys

Public keys are used to verify that a signed message was signed by a particular account/user
Addresses in a blockchain are some derivative of the public key

#### Signing Transactions

A "one way" process. Someone with a private key signs a transaction by their private key being hashed with their transaction data
Anyone can verify this new transaction hash with your public key

## Gas Optimizations

EIP-1559 specific to ethereum
Changing the Gas Limit allows you to pick when your transaction gets computed
The smallest unit of gas is called Wei which is 1^e-18 units of ether
Gwei or 10^9 Wei
Part of each ethereum transaction burns the some ether and tips the rest of the gas to the miner
Gas price varies by the congestion of the network which is based on the current demand in the blockchain

## Consensus

Consensus is the mechanism used to agree on the state of a blockchain

1. Chain Selection
2. Sybil Resistance
   - A blockchains ability to defend a user to get a disproportionate amount of control over the blockchain
   - Two main types
     1. PoW (Proof of Work)
        - Nodes compete to solve a problem, or mine, to compute the next block for the blockchain
        - Chain selection is also used by choosing the longest chain to avoid wasting extra computations
        - In PoW nodes are called Miners
     2. PoS (Proof of Stake)
        - Nodes put up collateral to prove that they will behave honestly
        - If they misbehave some of their stake will be slashed
        - In PoS nodes are called Validators
        - Nodes are randomly chosen to compute the next block and Validators are used validate the block
   - Common Attacks
     1. Sybil Attacks
        - Owns
     2. 51% Attack
        - Allows any user to control the blockchain network by having over 51% of control
        - The bigger the blockchain becomes the harder it is to have a 51% attack to occur

## Layer 1

## Layer 2

# Ethereum 101 (Block 1)

## Turing Complete

1. Turing-Complete

   - programming languages such as C or C++
   - TODO

2. Smart Contracts
   - Used to write decentralized applications or Dapps
   - Similar to classes in OOP

State -> Rule -> State'

Any State/Rule -> Any Application

## Infrastructure

1. Open-Source

   - The code and protocol are open source meaning that anyone can see the code that from any project

2. Blockchain State

   - The state of the blockchain is changed by storing transactions and synchronized by different blocks

3. Ether

   - The native currency used to meter & constrain prices of the blockchain

4. World Computer

   - The Ethereum Projects ultimate goal

## Properties

1. Permissionless Apps

   - Built-in Economics
   - No Permission needed to build or use projects

2. High Availability & High Auditability

   - The Network is always up
   - The fact that it is decentralized allows any transaction to be viewed by any block explorer

3. High Transparency

   - Neutrality
   - Allows any user to view any transaction made executed

4. Censorship Resistant

   - Low counter-party risk
   - Does not give entity too much power to remove and have full access control

## Purpose

1. Not a Currency

   - Ethereum is the network and ether is the currency you use to utilize the network

2. Ether

   - Needed to operate within the Ethereum Network

3. Utility Token

   - Used for every transaction or operation

4. Usage
   - The Ethereum network is used and you pay ether to use it

## Ethereum Vs. Bitcoin (Scripting)

1. Language

   - Bitcoin uses script instead of solidity

2. About Script

   - Script -> true/false
   - Spending conditions

3. Script compared to EVM
   - The EVM is turing complete meaning that when solidity code is compiled the code can be general purpose

## Ethereum Vs. Bitcoin (Blockchain)

1. Bitcoin Blockchain

   - Bitcoin focuses on the ownership of Bitcoin

2. Bitcoin UTX0

   - Only focused on Transfers of Bitcoin

3. Ethereum Blockchain

   - Focuses on more general-purpose state

4. Ethereum Account/Balance
   - Ethereum is much more account based than transaction based

## Core Components

1. P2P Network

   - TCP Port 30303: DEVp2p

2. Transactions

   - Transactions contain info such as: Sender, recipient, value, data

3. State Machine

   - The EVM is used to keep track of the state of the blockchain
   - The High level language solidity is used to compile code that the EVM can read

4. Consensus Algorithm

   - Nakamoto Consensus
     - P2P nodes need to agree what is the canonical blockchain that will be used
   - PoW (Proof of Work)
     - Used to determine which entity on the ethereum blockchain will be used to add the next block on the blockchain
     - Nodes are called Miners
     - Used as a method for Sybil Resistance
   - PoS (Proof of Stake)

     - Ethereum 2.0 has transitioned to proof of stake
     - Validators are used instead of miners to validate the state of the blockchain
     - ETH must be staked to be considered a Validator Node

   - Economic Security

     - If 51% of the blockchain has been accessed then then previous transactions can be altered

   - Clients
     - Geth, Erigon, Nethermind, OpenEthereum
     - Used to interact with the Ethereum Network

## Halting Problem

1. Turing Complete

   - The halting problem is that turing complete programming languages normally have programs that can predict or stop the program

2. Arbitrary Program/Input

   - Smart Contracts are designed to run forever

3. Smart Contracts

   - Smart Contracts need to predict how long until you can stop

4. Constrain Resources
   - Gas is used as a metering mechanism to constrain the amount of resources allocated to a Smart Contract

## Gas Metering

1. EVM

   - The EVM uses smart contract instructions called bytecodes that are each given a gas cost
   - The amount of Gas used depends on the amount of instructions used by the smart contract operations

2. Transaction

   - There is a Gas Limit that restrains the amount of resources that any bytecode can be accessed

3. Gas Exceeding Limit

   - EVM terminates when gas limit is exceeded by any operations

4. Turing Complete
   - Ethereum becomes turing complete by limiting the amount of Gas used by any operation

## Gas Mechanism

1. Transaction
   - Gas Price is measured in ether
2. Gas Price

   - Not Fixed /Varies
   - Depends on Demand
   - Gas Unit is similar to gas in cars

3. Gas Purchase

   - Purchase Transaction
   - Execute

4. Gas Consumed Remaining
   - Remaining gas gets refunded to sender

## Decentralized Application (DApp)

1. Decentralized Application

   - Web App Frontend combined with P2P infrastructure

2. P2P

   - Compute, Storage or Network

3. DApp

   - Web App + Smart Contract

## Web 2.0 Vs Web 3.0

1. Web 2.0

   - Client-Server existing infrastructure

2. Web 2.0 - Centrally Managed

   - Freemium/Ad Business Models

3. Web 3.0 - P2P

   - Compute/Storage/Network

4. Decentralized Incentivized Participation

   - Business Models apply for users, developers, and transactions
   - Crypto Economics
   - No Real Centralized management

## Ethereum Triad

1. Ethereum

   - Compute

2. Swarm

   - Storage

3. Whisper/Waku

   - Network

4. Triad

   - Ethereum & Swarm & Whisper/Waku

## Decentralization

1. Architectural

   - Physical Computers (Hardware)

2. Political

   - Individual/Organizations (Webware)

3. Logical

   - Data Structures (Software)

## Native Currency

1. Ether

   - Divisible up to 18 decimals

2. Smallest Unit

   - 10\*\*18 Wei = 1 ETH

3. Other Units
   - 10\*\*3 Wei = 1 Babbage
   - 10\*\*6 Wei = 1 Lovelace

## Cryptography

1. Public Key Cryptography (Asymmetric Cryptography)

   - Public-Private key pairs
   - Private key is made in a one way fashion by public key

2. Digital Signatures

   - Mainly used in Ethereum for signing transactions, not encryption

3. ECSDA (Elliptic Curve Digital Signature Algorithm)

   - Elliptic Curve Cryptography (ECC)

4. SECP-256K1 Curve

   - Elliptic Curve Finite Fields

5. Private Key
   - Secret Key (256-bit)
   - Random Number
   - Used to derive the public key
   - Public key used to derive Ethereum Address/Account

## Public Key

1. Not Secret

   - Public, For anyone to see

2. Private Key

   - Private key used to derive public key

3. Elliptic Curve Point

   - Multiplication

4. Public Key Derivation
   - Fundamentally public key must be derived from private key
   - If not then security of Ethereum would be fundamentally flawed

## Ethereum State

1. State

   - Accounts have unique address

2. Account
   - 20 byte address derived from public key
   - Transfer of value & information

## Ethereum Account

1. Nonce

   - Counter used to prove that each block can only exist once

2. Balance

   - Amount of ETH

3. Code

   - The code of the smart contract

4. Storage
   - The storage from internal smart contract state

## Account Types

1. Externally Owned Account

   - An account that is controlled by a private key
   - Anyone with private key can use ETH balance to use
   - Create digital signatures from account
   - Used to transfer value
   - Can execute smart contracts

2. Contract
   - Account controlled by code
   - Smart contract code and storage associated
   - Receive Tx/Message Run code & Access Storage
   - Message accounts and create contracts
   - ETH balance
   - Contract storage

## Keccak-256

1. Cryptographic Hash Function

2. SHA-3

   - Related to Keccak-256
   - Secure Hash Function (NIST, 2015)

3. Fundamental Primitive

## EOA Address

1. Private Key

   - Keccak-256(Public Key) and use 20 LSB
   - Last 20 bytes are used for EOA account

2. Transaction
   - Signed Message
   - Origin -> EOA
   - Trigger -> State Change
   - Transmitted -> Network
   - Recorded -> Blockchain

## Transaction Properties

1. Atomic

   - All or nothing
   - Cannot be divided/interrupted

2. Serial

   - One after another
   - Sequentially -> No parallelism

3. Inclusion

   - Miners, Congestion in Network, gasPrice

4. Order
   - Decide order of transactions within a block

## Transaction Components

1. Serialized Binary Message

   - Nonce -> sequence number changes

2. Gas Price

   - Wei/ Gas Unit
   - Gas Limit = max gas

3. Recipient

   - Destination address value
   - Received in Wei

4. Data
   - Payload
   - v,r,s = ECDSA Signature

## Nonce

1. Number Used Only Once

2. Sequence Number

   - Prevent replay attacks

3. EOA

   - Number of transactions sent from account

4. Contract
   - Number of contracts created from account

## Gas Price

1. Gas Price

   - Originator willing to pay

2. Wei

   - Gas Unit

3. Higher

   - Faster block inclusion by miner

4. Price
   - Demand block
   - Limit

## Gas Limit

1. Max Gas Units

   - Max Originator is willing to pay

2. Ether Transfer

   - 21,000 gas at least

3. Contract Tx

   - More Gas, Less Gas
   - OOG Error, Out of gas error

4. Estimated Gas
   - TX Excess Gas
   - Sent Back

## Recipient

1. 20-Byte Address

   - TX Recipient

2. EOA Address

   - Contract Address

3. Any Address

   - No Protocol Validation

4. No From Address
   - v,r,s -> Public Key -> Address

## Value

1. Value of ETH

   - Sender to recipient

2. EOA

   - Balance increase sender
   - Balance decrease

3. Contract
   - Data?
     - Contract function
   - No data
     - Receive/Fallback function
   - Exception
     - Called if no receive or fallback function

## Data

1. Data

   - Sender to recipient
   - Contract Account
   - Function Args

2. Recipient
   - Contract account

## V,R,S

1. ECDSA Signature

   - 65 bytes

2. r,s

   - signature component
   - 32 bytes each

3. v
   - recovery id
   - 1 byte
   - 27/28 or
   - chainId\*2 + 35/36

## Signature Purpose

1. Authorization

   - Auth for ether or to execute contract

2. Non-repudiation

   - Auth is undeniable

3. Integrity
   - Tx Data X -> Modified

## Contract Creation

1. Creation Transaction

   - sent to 0 address
   - data is contract bytecode
   - value -> contract balance

## TXs Vs Messages

- Tx: Offchain -> OnChain
- Msg: Onchain -> OnChain

1. Tx

   - Triggers Msg
   - ETH Transfer or Contract Code

2. Msg
   - Triggered by EOA Tx
     - EOA -> EOA or Contract
   - Triggered by EVM Call
     - Contract -> Contract

## TXs & Blockchain

1. Transactions
   - Grouped together to form block
   - Blocks linked together
   - Linked blocks are called blockchain

## Block

1. Block

   - Grouped transactions

2. Hash

   - Previous block

3. Block Change
   - Affects all following blocks
   - Every block created has reference to previous block

## Ethereum Node/Client

1. Node

   - Protocol implement Ethereum Specification

2. P2P

   - Node to node

3. Client
   - Specific implementation
   - Geth, OpenEthereum, Nethermind, Erigon

## Ethereum Miners

1. Entities

   - Running Ethereum Nodes

2. Transactions

   - Validate/Execute/Combine
   - Blocks

3. Block Validation

   - PoW previously
   - Now PoS

4. Block Reward
   - 2 ETH
   - Tx Fees from All block Txs

## Block Gas Limit

1. Total Gas Spent

   - All TXs in Block

2. TXs -> Block

   - Caps -> number transactions in block

3. Block size X

   - Fixed number transactions Gas/Tx
   - Gas limit

4. Set -> Miners
   - Current 15 million

## GHOST

1. Miners

   - blocks
   - network propogation

2. Multiple Valid Blocks

   - chooses one using GHOST
   - Greedy Heaviest Observed Subtree Protocol (GHOST)

3. Canonical Blockchain
   - State blocks -> Ommers

## Consensus

1. Nakamoto Consensus

   - Next block -> which miner?
   - PoW
   - Longest Chain Rule

2. Ethereum State

   - Address -> Account State
   - Modified merkle-patricia Tree / Binary Tree

3. Leaf Nodes
   - Data
   - Intermediate Nodes -> Hash (Two Child Nodes)
   - Single root node -> Root Hash
   - Each node has 16 children

## Ethereum PoW

1. Ethash
   - (m,n) = PoW(H_n,H_n, d)
   - m = H_m ^ n <= 2\*\*256/H_d
   - n: nonce, H_d - Difficilty
   - m: mix hash, d: Data Set

## Block Header

1. Block
   - Header, Txs, Ommers' Headers
   - Block Header
     - parentHash
     - ommersHash
     - beneficiary
       - Address controlled by miner
   - stateRoot
   - transactionRoot
   - receiptsRoot
   - logsBloom
   - difficulty
   - number
   - gasLimit
   - gasUsed
   - extraData
   - timestamp
   - mixHash
   - nonce

## State Root

1. 256-bit hash

   - Modified merkle-patricia Tree

2. Leaves

   - Key-Value Pairs
   - Address -> account

3. Account

   - Nonce
   - Balance
   - codeHash
   - storageRoot

4. codeHash: hash(Code)
   - storageRoot: Account Storage

## Tx Receipt

1. Tuple
   - Cumulative gas used
   - Tx
     - Set of logs
   - Logs
     - Bloom Filter
   - Tx Status Code

## Tx Gas

1. Beneficiary

   - Credited with miner TX fees

2. Gas Refund

   - Tx gasLimit - Gas Used

3. Refund

   - Sender Same gasPrice

## EVM

- Ethereum Virtual Machine
- Smart Contracts
  - Execute in Runtime Environment
- Quasi Turing Complete
- Turing Complete
  - Gas Bounded Computation

## Ethereum Code

1. EVM
   - Low-level & Stack-based
     - EVM Machine Code
   - Series of Bytes
     - Byte Code
   - One Byte
     - One Operation

## EVM Architecture

1. Stack-based Architecture
   - stack volatile memory
   - non-volatile storage
   - calldata
   - word size
     - 256-bits
     - Keccak-256 & ECC

## Stack

- 1024 Elements
  - 256-bits
- Most EVM Operations
  - Stack Elements
- Stack-based architecture
  - Top 16 Elements
- Stack-specific operations
  - PUSH/POP/SWAP/DUP

## Memory

1. Volatile Memory

2. Linear Byte Array

   - Byte-level addressable

3. Zero-initialized

4. MLOAD/MSTORE/MSTORE8

## Storage

1. Non-volatile Storage

   - Persistent across transactions on blockchain

2. Key-Value Store

   - 256-bit <-> 256-bit

3. Zero-initialized

- storageRoot -> stateRoot

4. SLOAD/SSTORE
   - SLOAD
     - Loads words from storage and puts it on the stack
   - SSTORE
     - Stores word from stack and puts it into storage

## Calldata

1. Data Parameters

   - TXs & Message Calls

2. Read-Only

   - Byte-addressable

3. Three Instructions
   - CALLDATASIZE
   - CALLDATALOAD
   - CALLDATACOPY

## EVM Architecture

1. Von Neumann Vs Harvard

2. Code & Data

3. Memory & Pathways

   - Together or Separately

4. EVM Code
   - Virtual ROM
   - Special Instructions

## EVM Ordering

1. Big-Endian Vs Little-Endian

2. Big-Endian

   - EVM is Big-Endian

3. MSB

   - Lowest Address

4. LSB
   - Highest Address

## Instruction Set

1. Eleven Categories
   - Stop and Arithmetic
   - Comparison & Bitwise Logic
   - SHA3
   - Environmental Information
   - Block Information
   - Stack, Memory, Storage & Flow
   - Push
   - Duplication
   - Exchange
   - Logging
   - System

## Stop and Arithmetic ISAs

- 0x00 STOP n1 n2
- 0x01 ADD n1 n2
- 0x02 MUL n1 n2
- 0x03 SUB n1 n2
- 0x04 DIV n1 n2
- 0x05 SDIV n1 n2
- 0x06 MOD n1 n2
- 0x07 SMOD n1 n2
- 0x08 ADDMOD n1 n2
- 0x09 MULMOD n1 n2
- 0x0A EXP n1 n2
- 0x0B SIGNEXTEND n1 n2

## Comparison & Bitwise Logic ISAs

- 0x10 LT n1 n2
- 0x20 GT n1 n2
- 0x12 SLT n1 n2
- 0x13 SGT n1 n2
- 0x14 EQ n1 n2
- 0x15 ISZERO n1 n2
- 0x16 AND n1 n2
- 0x17 OR n1 n2
- 0x18 XOR n1 n2
- 0x19 NOT n1 n2
- 0x1A BYTE n1 n2
- 0x1B SHL n1 n2
- 0x1C SHR n1 n2
- 0x1D SAR n1 n2

## SHA3

- 0x20 SHA3 n2 n1
  - Compute Keccak-256 Hash

## Environmental Information

- 0x30 ADDRESS 0 1
- 0x31 BALANCE 1 1
- 0x32 ORIGIN 0 1
- 0x33 CALLER 0 1
- 0x34 CALLVALUE 0 1
- 0x35 CALLDATALOAD 0 1
- 0x36 CALLDATASIZE 0 1
- 0x37 CALLDATACOPY 0 1
- 0x38 CODESIZE 0 1
- 0x39 CODECOPY 0 1
- 0x3A GASPRICE 0 1
- 0x3B EXTCODESIZE 0 1
- 0x3C EXTCODECOPY 0 1
- 0x3D RETURNDATASIZE 0 1
- 0x3E RETURNDATACOPY 0 1
- 0x3F EXTCODEHASH 0 1

## Block Information

- Information
  - Transaction's Block
- 0x40 BLOCKHASH 0 1
- 0x41 COINBASE 0 1
- 0x42 TIMESTAMP 0 1
- 0x43 NUMBER 0 1
- 0x44 DIFFICULTY 0 1
- 0x45 GASLIMIT 0 1

## Stack Memory, Storage, and Flow

- 0x50 POP 1 0
- 0x51 MLOAD 1 1
- 0x52 MSTORE 1 0
- 0x53 MSTORE8 1 0
- 0x54 SLOAD 1 0
- 0x55 SSTORE 1 0
- 0x56 JUMP 1 0
- 0x57 JUMP1 1 0
- 0x58 PC 0 1
- 0x59 MSIZE 0 1
- 0x5A GAS 0 1
- 0x5B JUMPDEST 0 1

## Push Operations

- Place Items
  - Stack
- 0x60 PUSH1 0 1
- 0x61 PUSH2 0 1
- PUSH3, PUSH4, PUSH5 ...., PUSH31
- 0x7F PUSH32 0 1

## Duplication Operations

- Duplicate Items
  - Stack
- 0x80 DUP1 1 2

## Exchange Operations

- Exchange Items
  - Stack
- 0x90 SWAP1 2 2
- SWAP2, SWAP4, .... SWAP15

## Logging Operations

- Append Log Record
  - Topics
- 0xA0 LOG0 2 0
- 0xA1 LOG1 3 0
- 0xA2 LOG2 4 0
- 0xA3 LOG3 5 0
- 0xA4 LOG4 6 0

## System Operations

- 0xF0 CREATE 3 1
- 0xF1 CALL 7 1
- 0xF2 CALLCODE 7 1
- 0xF3 RETURN 2 0
- 0xF4 DELEGATECALL 6 1
- 0xF5 CREATE2 4 1
- 0xFA STATICCALL 6 1
- 0xFD REVERT 2 0
- 0xFE INVALID 0 0
- 0xFF SELFDESTRUCT 1 0

## Gas Costs

- Diff Instructions
  - Different costs
  - Computational/Storage Load
- STOP/INVALID/REVERT: 0
- Most Arithmetic/Logic/Stack: 3-5
- CALL*/BALANCE/EXT*: 2600
- MLOAD/MSTORE/MSTORE8: 3
- SLOAD: 2100
- SSTORE: 20000/5000
- CREATE: 32000
- SELFDESTRUCT: 5000

## Transaction Reverts

- Different Exceptional Conditions
- E.G: Out of Gas, Invalid Instructions
- State Changes
  - Discarded
- Original State
  - Restored
- As if Tx X
  - Executed

## Transaction Data

- Recipient
  - Contract Address
- Tx Data
  - Target Function & arguments

## ABI

1. Application Binary Interface

2. Required

   - Interact with Contracts

3. Interface Functions

   - Strongly Typed

4. Known
   - Compile Time & Static

## Function Selector

1. Selector

   - Contract Function

2. First 4 bytes

   - Keccak256(Fn Sig)

3. Fn Sig

   - Name(param1_type, param2_type)

4. Fn Args
   - Encoded & 5th Byte Onwards

## Block Explorer

1. Application

   - Web Portal

2. Real-time On-Chain Data
   - Blocks & Transactions
   - Accounts
   - Interactions
   - Gas
   - Balances
   - Calls
   - i.e Etherscan, Etherchain, Ethplorer, Blockchain, Blockscout

## Mainnet

1. Mainnet

   - Main Ethereum Network

2. Mainnet Vs Testnets

   - ETH Vs Faucet Test ETH

3. Sepolia
   - PoA Testnet
   - PoA: Proof of Authority

## EIP

1. Ethereum Improvement Plan

   - EIP

2. Standards & Specifications

3. Core, Networking, Interface, ERC(e.g. ERC-20)

4. Meta & Informational

## ETH 2.0.

1. Ethereum 2.0.

   - Biggest Upgrade

2. More Scalable Sharding

3. More Secure

   - Proof of Stake

4. More Sustainable
   - PoW -> PoS

## Immutable Code

1. Immutable Contracts

   - Bugs X -> Fix

2. Contract

   - Redeployed

3. Upgradeable Proxy

   - Can introduce security risks if not done properly

4. CREATE2

## Web 3.0.

1. Permissionless

   - Trust-minimized
   - Censorship-resistant

2. P2P: Compute/Storage/Network

   - Ethereum/Swarm/Waku

3. Privacy & Anonymity

4. Web2 Principles & Practices
   - Paradigm Security Shift

## Languages

1. Web2

   - JS, Go, Rust, Nim, C, C++

2. Web3

   - Web + Smart Contracts

3. Smart Contracts

   - Solidity, Vyper, Others WIP

4. Solidity
   - Most Used

## Onchain Vs Offchain

1. Web2

   - Offchain
   - Outside of Blockchain

2. Web3

   - Offchain + Onchain

3. Security

   - Offchain + Onchain

4. Main Differences
   - Onchain -> Smart Contracts

## Open-source & Transparent

1. Open-Source

   - By Default
   - Verified Contract

2. Txs & State

   - Public Real-time
   - Historical

3. All Txs

   - Blockchain Pending Txs
   - Mempool

4. No Security By Obscurity

## Unstoppable & Immutable

1. Dapps

   - Decentralize Infrastructure & Governance

2. One Entity

   - Stop
   - Change Dapps/Infra/Gov

3. Contracts

   - Change/Stop
   - Upgrade or Kill Switch

4. Harder
   - Fix Vulnerability
   - Incident Response

## Pseudonymity & DAOs

1. Regulatory & Uncertainty

   - Legal implications

2. Reputation

   - Trustworthiness

3. Legal/Social Accountability

   - Wetware Vs Software

4. DAOs
   - Decision making security implications

## Arch & Lang & Tools

1. Ethereum & EVM

2. Solidity, Vyper & More

3. Hardhat, Truffle, Brownie, OpenZeppelin & More

4. Slither, MythX, & More

## Byzantine Threat Model

1. Web2

   - Insiders/Outsiders
   - Trusted/Untrusted

2. Web3

   - Byzantine Fault Tolerance

3. Arbitrarily Malicious Mechanism Design

4. Untrusted By Default
   - Users
   - Abusers

## Key & Tokens

1. Passwords Vs Keys

2. Reset/Restore Vs Permanent Loss

3. Data Vs Tokens

4. Fines/Reg/Reversals Vs Irreversible/Immutable

## Composability

1. Open/Composability By Design

2. Permissionless Access Users/Contracts

3. Components, Configs & Dependencies

4. Vulnerabilities, Exploits & Attack Surface

## Timescale

1. Compressed Timescales

2. Open-source & Composable Permissionless & Borderless

3. Token Incentivized & Execution Speed

4. Security X
   - Design & Dev Vulnerabilities & Exploits

## Test-in-Prod

1. Compressed Timescale

   - Unrestricted Composability

2. Byzantine Threat Model

   - Full-state replication

3. Experimental Tools

   - Mechanism Design

4. Real-World Failure Models
   - Mainnet

## SSDLC

1. Secure Software Development Life-Cycle

2. Web2

   - SSDLC

3. Web3

   - Audits

4. Build -> Audit -> Launch

5. Audit-as-a-Silver-Bullet

## State of Audits

1. External Assesment

   - Security Approval X -> Stamp

2. In-house X -> Expertise External Audit Firms

3. Unreal Expectations

   - Very Expensive

4. Demand >> Supply
   - Increase/Train Auditors

# Solidity 101

Focus is on high-level conecepts to the solidity basics

## Solidity

1. High-level Language for Ethereum

2. Smart Contracts Targets EVM

3. 2014: Gavin Wood, Christian Reitwiessner

4. Fundamental Pillar
   - Few Alternatives

## Influence

1. Main

   - C++

2. C++

   - Syntax, OOP, Etc.

3. Python

   - Modifiers, super, Etc.

4. Javascript
   - Scoping, Var
   - Early, Not anymore

## Features

1. Language Characteristics
   - Curly-bracket language
   - Object-oriented language
   - Statically-typed
   - Inheritance (OOP)
   - Libraries
   - User-defined types
   - Fully-featured high-level language

## Layout

1. Solidity Source File Layout
   - Pragma/Import Directive
   - Struct/Enum
   - Contract Definitions
   - Contract Order Best Practice
     - Struct/Enum
     - State Variables
     - Events
     - Errors
     - Modifiers
     - Constructors
     - Functions

## SPDX

1. License Identifier
   - Software Package Data Exchange
   - Comment
     - License File Beginning

## Pragma

1. Compiler Features/Checks

   - Ex: pragma solidity ^0.8.0
   - Two Checks
     - Version
     - ABI Coder
   - Every File Not Imported

2. Version Pragma
   - Solidity Compiler Version
     - pragma solidity x.y.z
   - Checks Used Vs Specified
     - Simple
     - Complex
     - Floating
       - Introduces ^
       - Means can be compiled with any compiler version above specifed version
   - Different z
     - Bug Fixes
   - Different y
     - Breaking Changes
   - Affects
     - Features
     - Optimizations
     - Security
3. ABI Coder

   - ABI Coder Pragma Version
     - v1 or v2
   - v2
     - Encode/Decode nested Arrays/Structs
   - v2 Superset v1 File of Definition/Use
   - Affects
     - Features
     - Optimizations
     - Security

4. Experimental
   - ABI Expiremental
     - SMTChecker
   - Not Enabled By Default
     - Safety Checks
       - SMT Solver
   - Checks
     - require/assert
     - Overflow/Underflow
     - Div/0
     - Unreachable Code
     - Etc.
   - Affects
     - Security
     - Optimizations

## Imports

1. Import Statements

   - Ex
     - Similar to JS import FILE_NAME

2. Code Modularity

   - Code Reuse

3. Affects
   - Readability
   - Security
   - Optimizations

## Comments

1. Inline Comments

   - Single Line
     - Ex: //
   - Multi-line
     - Ex: /_ ... _/

2. Implement

   - Document assumptions/invariants

3. Readability/Maintainability

## NatSpec

1. Ethereum Natural Language Specification Format

   - /// or Double asterisk

2. Tags
   - @title
   - @author
   - @notice
   - @dev
   - @param
   - @return
   - Used as JSON Doc for Users

## Contracts

1. Contracts

   - Similar to Classes in OOP

2. State

   - Variables

3. Modification

   - Functions

4. Other Contracts

   - Inherit
   - Interact

5. Fundamental Primitives

## Contracts

1. Contracts

   - Components
   - Struct/Enum
   - State Variables
   - Events
   - Errors
   - Modifiers
   - Constructor
   - Functions

2. Contracts
   - Libraries
   - Interfaces

## Variables

1. State Variables

   - All Contract Functions Can Access

2. Data Location

   - Contracts Storage

3. State Variables
   - Contract State

## State Visibility

1. State Visibility Specifiers

2. Public

   - Interface
   - Internally/Externally
   - Getter

3. Internal

   - Current/Derived
   - Similar to the protected variable in C++

4. Private

   - Can only be accessed from contract where variable is defined

5. Contract
   - Interface/Interactions

## State Mutability

1. State Mutability Specifiers

2. Constant

   - Fixed at Compile-time
   - Value is the same for the life of the contract

3. Immutable

   - Fixed at construction-time
   - Can be assigned when deployed

4. No Storage Slot
   - No storage slot
   - Storage/Gas Efficient

## Mutability & Gas

1. State Mutability Gas Costs

2. Constant

   - Copied @Usage
   - Local Optimizations

3. Immutable
   - Evaluated Once & Copied
   - 32bytes are reserved even if not used

## Functions

1. Contract Functions

2. Executable Units of Code

3. Inside Contracts

   - File-level
     - Free

4. Functions
   - State
     - Modifications
     - Transitions

## Parameters

1. Function Parameters

2. Declared

   - As Variables

3. Used/Assigned

   - Lcoal Variables

4. Caller

   - Arguments

5. Callee
   - Parameters

## Return Variables

1. After returns keyword

2. Single or Multiple

   - Named or Unnamed

3. Like local Variables

   - return Statement

4. Caller

   - Callee

5. Parameters
   - Return Value

## Modifiers

1. Function Modifiers

   - Modifier Keyword

2. modifier mod()
   - {Checks; \_;}
   - Ex
   - function foo() mod {}
     - mod -> foo()
3. Pre-conditions

   - Access Control

4. Post-conditions
   - Accounting

## Function Visibility

1. Public/External/Internal/Private

2. Public/External

   - Interface

3. External

   - Not Internally

4. Internal

   - Base/Derived

5. Private

   - Contract

6. Visibility
   - Access Control
   - Security Implications

## Function Mutability

1. View or Pure

2. View

   - Read State
   - Not Modity
     - Use STATICCALL Op Code

3. Pure

   - Not Modify
   - Not Read
     - Not from EVM

4. Mutability

   - Write/Read
   - Security Implications

## Function Overloading

1. Multiple Functions

   - Same Name
   - Different Parameters

2. Function Arguments

   - Match Declarations in Scope

3. Return Variables

   - Not Considered

4. Overloading
   - OOP

## Free Functions

1. Function Defined

   - Outside Contracts

2. Contract Functions Vs Free Functions

3. Code Included in All Calling Contracts

4. Similar

   - Internal Library

5. Functions
   - Rarely Seen

## Events

1. EVM Logging Abstraction

2. Event

   - Emit

3. Contract Log

   - Blockchain

4. Contracts

   - No Access

5. Off-chain

   - RPC Access

6. Auditing & Logging
   - Security Monitoring

## Indexed Parameters

1. Event Parameters

   - Indexed or Not

2. Indexed

   - Topics

3. Not Indexed

   - Data

4. Topics
   - Search/Filter
   - Up to 3 parameters
   - Indexed
     - ERC-20 Spec
   - Gas
     - Fast Search

## Emit

1. Events Declaration

   - Emit

2. Emit
   - Event Log
   - Ex
     - emit Deposit(msg.sender, \_id, msg.value)
3. Emit Correct Event
   - Emit Correct Parameters

## Structs

1. Custom Data Structures

2. Several Variables

   - Different Types

3. Struct Members

   - . Access
   - E.g.
     - s.user
     - s.amount
   - Aggregate Type
   - Commonly Used

4. Enums

   - Used-defined Type
   - Finite-set
     - Constant Values
     - Min: 1
     - Max: 256

5. Improves Readability

## Constructor

1. Contract Creation

   - Constructor Function

2. Optional & Only One

   - Constructor Keyword

3. Initialize State

   - Contract Code
     - Stored on Blockchain

4. Initializations Vs Defaults
   - Affects Security

## Receive Function

1. Ether Transfers

   - send/transfer
   - Empty Calldata

2. One Function

   - only one function per contract
   - No Parameters/return
   - External
   - Payable

3. send/transfer

   - 2300 Gas

4. Security
   - ETH Balance
     - Assumptions

## Fallback Function

1. No Match

2. No Data

3. No Receive

4. One Function
   - only one function per contract
   - External
   - Payable for ETH
5. send/transfer

   - 2300 Gas

6. Security
   - ETH Balance
     - Assumptions

## Statically Typed

1. Variable Types

   - Specified compile-time

2. Vs Dynamically-typed
   - Types
     - Run-time Values
3. Compile-Time

   - Type Checking

4. Other Examples
   - C, C++, Java, Rust, Go

## Types

1. Value & References

2. Value

   - Passed by Value
   - Copied
     - Arguments/Assignments

3. Reference
   - Passed by Reference
   - Multiple Names
     - Same Variable
4. Security
   - State Updates/Transitions

## Value Type

1. Types

   - Value
   - Reference
   - E.g
     - Bool
     - Integer
     - Address
     - Enums
     - Etc.

2. Security
   - Copy
     - Safer
   - Check
     - Persistence

## Reference Type

1. Types

   - Value
   - Reference
   - E.g.
     - Arrays
     - Structs
     - Mappings

2. Security
   - Risky
   - Unintentional Modification

## Default Values

1. Variable

   - Declared
   - Not Initialized

2. Default

   - Zero-state of Type
   - E.g.
     - Bool: False
     - Integer: 0
     - Address: 0
     - Enum: First Member

3. Security
   - Important
   - E.g.
     - Address Burn

## Scoping

1. Variable Visibility

   - C99 Scoping

2. Declaration

   - End of {}
   - Parameter
     - Code Block

3. Functions/Contracts/State
   - Variables
     - Visible Before Declaration
4. Security
   - Data Flow Analysis

## Boolean

1. Bool Keyword

2. True or False

   - Operators
     - !
     - ==
     - !=
     - &&
     - ||

3. Short-Circuit

   - ||
   - &&
   - Evaluate leftmost argument first to reduce Gas

4. Security
   - Control Flow
   - Checks
   - || Vs &&

## Integers

1. Uint/Int keywords
   - Sizes: 8 -> 256 Bits
   - E.g
     - uint8
     - uint16
     - uint256
2. Operators

   - Arithmetic
   - Comparitive
   - Bit
   - Shift

3. Security
   - Data Flow
   - Under Flow
   - Over Flow

## Integer Arithmetic

1. E.g

   - uint256
   - Range: 0 - 2\*\*256-1

2. Underflow/Overflow

   - Wrapping

3. Solidity < 0.8.0

   - Use safeMath from OpenZeppelin

4. Solidity >= 0.8.0
   - Checked Vs Unchecked

## Fixed Point

1. Fixed Vs Floating

2. Keyword

   - fixed & ufixed

3. Solidity

   - No real support

4. Libraries
   - DSMath
   - PRBMath
   - ABDKMath64x64
   - Etc.

## Address

1. Account Address
   - EOA
   - Contract
   - Not Variable Memory Address
     - Like in C++, C
2. Keyword

   - Account (payable)
   - 20 Bytes

3. Operators

   - ==
   - !=
   - <
   - <=

4. Security
   - Critical
   - Access Control
   - Balances
   - Etc.

## Address Members

1. Balance

2. Code

3. Codehash

4. Transfer & Send

   - 2300 Gas Stipend

5. Call

6. Delegatecall

7. Staticcall

8. Security
   - Balances
   - EOA/Contract
   - ETH Tx
   - External Calls

## Transfer

- Primitive

1. Ether Transfer

2. Transfer

   - Receive
   - Fallback
   - From Target Contract

3. 2300 Gas Subsidy Failure

   - Revert

4. Security
   - Reentrancy
   - Mitigation
   - Gas Assumption

## Send

- Primitive

1. Ether Transfer

2. Send

   - Receive/Fallback

3. 2300 Gas Subsidy

   - No Revert

4. Security
   - Reentrancy
   - Mitigation
   - Gas Assumption
   - Return Value Check

## External Calls

1. Call

2. Delegatecall

3. Staticcall

4. Parameter

   - bytes memory
   - Return
     - Success
     - Bytes Memory
   - Abi\*.
   - Functions
   - Gas/Value

5. Delegatecall

   - State/Modify

6. Staticcall

   - State/Use

7. Security
   - Low-level call
   - Untrusted Contract
   - Reentrancy
   - Return Value Check

## Contract Type

1. Every Contract

   - Own Type

2. Contract

   - Address

3. No Operators

4. Members
   - External Functions
   - Public State Variables

## Bytes Arrays

1. Fixed-size Byte Arrays

2. bytes1, bytes2, ...bytes32

3. bytes Vs byte[]

   - Wastage

4. bytes
   - Byte Storage
   - E.g.
     - Hashes

## Literals

1. Five Types

   - Address
   - Rational/Integer
   - String
   - Unicode
   - Hexadecimals

2. Address
   - 40 Hex & Checksum
   - Integer/Decimal
     - . & \_
3. String

   - ".."

4. Unicode

5. Hex

   - hex".."/hex'..'

6. Usage
   - Constants

## Enums

1. User-defined Types

2. Members

   - At least 2
   - Max 256

3. Default

   - First Member

4. Usage
   - E.g.
     - State Names
     - Transitions

## Function Types

1. Variables

   - Function Type

2. Assigned

   - Functions
   - Parameters/Return Value

3. Internal Vs External

4. Usage
   - Minimal

## Data Location

1. Reference Types

   - Data Location Annotation

2. memory

   - function

3. storage

   - contract

4. calldata

   - non-modifiable
   - non-persistent
   - external function parameters

5. Impact

   - Scope

6. Security
   - Persistence

## Data Location & Assignments

1. Data Location

   - Persistency & Assignment Semantics

2. Storage-memory

   - Copy

3. Memory-memory

   - Reference

4. storage-storage

   - Copy

5. Others

   - Copy

6. Impact

   - Copy/Modification

7. Security
   - Reference Risk

## Arrays

1. Static or Dynamic
   - Static
     - T[k]
   - Dynamic
     - T[]
   - Elements
     - Any Type
   - Indices
     - Zero-based
   - Access Past
     - Revert
2. Security
   - Correct Index
   - Off-by-one
   - Gas/DoS

## Array Members

1. length

   - Number or Elements

2. push

   - Zero Element @ End

3. push(x)

   - x @ end

4. pop

   - Remove element @ end

5. Security
   - Length
   - Off-by-one
   - push/pop semantics

## Bytes & String

1. Bytes

   - Byte data
   - Arbitrary data/length

2. bytes1, bytes2, ..bytes32

   - bytes over byte[]
     - Cheaper
   - byte[]
     - uses 31 bytes of padding for each element

3. String == bytes

   - No length
   - No Index Access

4. Solidity
   - No string functions
   - Third-party libraries availlable

## Memory Arrays

1. Memory Arrays

   - new Operator

2. Memory Vs Storage

   - Cannot Resize
     - No Push

3. Calculate Size
   - Calculate size in Advance
   - New Array
     - Copy Over other array
   - E.g.
     - uint[] memory = new uint[](7);

## Array Literals

1. Comma-separated list

   - withing [...]

2. Statically-Sized

   - Length = #Expressions

3. Type = First Element

   - Others Convertible

4. No Assignment to
   - Dynamically-sized array

## Arrays Gas Costs

1. push() & pop()

2. push

   - constant cost

3. pop

   - depends on element size

4. Pop Array Element
   - Expensive
   - Delete Element

## Arrays Slices

1. View

   - Contiguous Array Portion

2. x[start:end]

   - x[start] to x[end-1]

3. start & end
   - Optional
   - start <= end & end < length

## Struct Types

1. New Aggregate Type

2. Combine Value/Ref Types One Unit

3. Inside or Contain Mappings & Arrays

4. Cannot contain members of same type

## Mapping Types

1. Key-Value Pairs

   - mapping(key => value) var

2. Key Type

   - restricted

3. Value Type

   - Any

4. Key Value

   - Not Stored
   - Keccak256 Lookup

5. No Length/Set

   - Storage Only
   - No Iteration

## Shorthand Operators

1. LValues
   - Assigned To
2. Pre-Increment

3. Post-Increment

## Delete

1. Delete

   - Assigns Initial Value to a

2. Ints

   - 0

3. Dynamic Arrays

   - Length 0

4. Static Arrays

   - Same Length

5. Initial Value Elements

6. Arr[x]
   - Deletes Item @x
7. Structs

   - Members Reset Unless Mappings

8. Mappings

   - No Effect

9. Specific Key
   - Value @ Key Deleted

## Implicit Conversions

1. Type Conversion

   - Compiler Applied

2. Assignments/Arguments/Operators

3. Semantic Sense
   - No information lost
   - E.g
     - uint8 -> uint16
     - int128 -> int256

## Explicit Conversions

1. Type Conversion

   - Developer Applied

2. Unexpected Behavior

   - Bypass Type Safety

3. Smaller Type

   - Higher Order Cut-Off

4. Larger Type

   - Higer Order Padded

5. Fixed-Size
   - bytes1..bytes32

## Conversion Literals

1. Literals <-> Elementary Types

2. Decimals/Hex -> int

3. Hex -> Fixed-size byte arrays

4. IFF #HEX Digits Exactly fits

5. String/Hex String
   - Fixed-size byte arrays
   - IFF #Chars Exactly Fits

## Ether Units

1. Suffix

   - Literal Number
   - Wei, GWei, Ether

2. Wei

   - Base unit
   - 1 wei == 1
   - 1 GWei == 1e9
   - 1 Ether == 1e18

3. Suffix
   - Multiplication by power of 10

## Time Units

1. Suffix

   - Literal Number
   - Seconds/Minutes/Hours/Days/Weeks

2. Seconds

   - Base Unit
   - 1 == 1 Seconds

3. 1 days == 24 hours == 1440 Minutes == 86400 seconds

4. Variables -> Multiply

## Block & Tx Properties

1. Block:
   - Hash
   - ChainId
   - Number
   - Timestamp
   - Coinbase Address
   - Difficulty
   - GasLimit
   - Msg
     - Value
     - Data
     - Sender
     - Signature
   - Tx
     - GasPrice
     - GasLeft
     - Origin
       - Sender of Transaction, i.e. EOA

## Msg Values

1. Value

   - Wei Sent

2. Sender

   - Sender Address

3. External Call

   - Sender Changes
   - Value Can Change

4. Security
   - Assumptions

## Randomness Source

1. Miners Can Influence

   - block.timestamp
     - Timestamp(block) > Timestamp(block-1)
   - blockhash

2. Do Not Rely
   - Source of Randomness

## Blockhash

1. blockhash(blocknumber)

2. Hash of Given Block

3. Only 256 Recent Blocks

   - Excluding Current Block

4. All Other Values
   - Zero

## ABI Encoding/Decoding

- abi.encode(...)
- abi.decode(...)
- abi.encodeWithSelector(...)
- abi.encodeWithSignature(...)
- abi.encodePacked(...)
- Packed Encoding
  - Ambiguous

## Error Handling

1. assert(bool condition)

   - Panic/Revert

2. require(bool condition, [string memory message])

   - Error/Revert

3. revert([string memory message])

   - Abort/Revert

4. assert() vs require()
   - assert
     - Meant to be used for internal errors
   - require
     - Meant to be used for external errors
       - Ex. due to user inputs

## Math/Crypto Functions

1. addmod() & mulmod()

2. Keccak256(bytes memory)

3. sha256(bytes memory)

4. ripemd160(bytes memory)

5. ecrecover(bytes32 hash, uint8 v, bytes32 r, bytes32 s)
   - recovers address associated with public key

## ecrecover Malleability

1. Vulnerable to non-uniqueness

2. Two Valid Signatures

3. Signature Malleabillity
   - Replay attacks
4. Sig -> (v,r,s)
   - s Values
     - Lower Range
     - This is what allows Malleability
5. Unique Signatures
   - OpenZeppelin ECDSA

## Contract Related

1. this

   - Current contract
   - Convert
     - Address

2. selfdestruct

   - selfdestruct(address payable recipient)

3. selfdestruct(recipient)

   - Destroy Current Contract

4. Send Funds
   - Recipient End Execution

## selfdestruct

1. Peculiarities

2. Recipient Contract

   - receive() Not Executed

3. Contract Destroyed

   - End of Tx

4. Revert
   - Undo Destruction

## Contract Type

1. type(x)
   - x: Contract
   - type(c).name: Contract name
   - type(c).creationCode
   - type(c).runtimeCode
   - Interface I
     - type(I).interfaceId

## Integer Type

1. type(x)

   - x: Integer

2. type(T).min

   - Smallest Value of T

3. type(T).max
   - Largest Value of T
   - e.g.
     - type(uint8).max
       - returns 255

## Control Structures

1. Control Flow

2. if/Else

3. while/do

4. for/break/continure/return

5. () X

   - Omit

6. {}

   - Omit single statement Bodies

7. Non-boolean X

   - Boolean

8. No Conversion
   - E.g.
     - If(1)

## Exceptions

1. State-reverting Exceptions

2. Sub-call Exception

   - Bubble-up

3. Except

   - send/\*call

4. External Calls

   - try/catch

5. Caller

   - Selector+Data

6. Error(string)

   - Regular

7. Panic(uint256)
   - Assertions
   - Should not be present in bug-free code

## Low-level Calls

1. call/staticcall/delegatecall

2. Non-existent Account

   - Return True

3. Check Account Existence
   - Before call

## Assert

1. assert()

   - Panic(uint256)

2. Internal Errors

   - Check Invariants

3. Normal Code

   - No Panic

4. assert() Vs require()

## Panic

1. Panic Error Codes

2. 0x01

   - False Argument

3. 0x11

   - Overflow
   - Underflow

4. 0x12

   - div/mod by 0

5. 0x31

   - pop() Empty array

6. 0x32
   - Out-of-bounds array
   - Access..and Others

## Require

1. require()

   - Error([string])

2. Detect Runtime Invalid Conditions

   - E.g.
     - Input Validation
     - Return Value Checks

3. Message String
   - Optional

## Error

1. Error(string)
   - Ex
     - require(arg == False)
       - revert([string])
2. External Call

   - No Code

3. Receive ETH
   - No Payable
   - public Function/Getter

## Revert

1. revert CustomError(arg1..)

2. revert([String])

3. Abort Executions

   - Revert State Changes

4. Custom Error Vs String

## try/catch

1. try Expr [returns()]{..}

   - catch BLOCK {..}
   - External Call Failure

2. No Error

   - Success Block

3. Error

   - catch Block

4. Block?
   - Error Type

## Catch Blocks

1. catch Error(string reason)

2. catch Panic(uint errorCode)

3. catch (bytes LowLevelData)

   - Run if no error data is provided

4. catch

## try/catch State change

1. Success Block Vs Error Block

2. try/Success Block X

   - Revert
   - External Call X
     - State Change

3. catch/Error Block

   - Revert
   - External Call X
     - State Change

4. try/catch Revert
   - Deccoding/Low-level

## External Call Failure

1. Many Reasons

2. Error

   - Called Contract Cannot Assume

3. Error

   - Deeper Call chain
   - Callee Forwarder

4. OOG (Out of Gas)
   - Caller
     - 63/64th Gas

## Programming Style

1. Coding Convention

2. Style

   - Consistency
     - Function
     - Module
     - Project
   - Effects
     - Maintainability
     - Readability

3. Layout & Naming

4. Code Layout
   - Indentation
     - 4 spaces
   - Spaces over Tabs X
     - Mix
   - Blank lines
     - 2
   - Max Line Length
     - 79/99
   - Wrapped Lines
     - src File
       - UTF-8/ASCII
   - Imports
     - top
   - Functions
     - contructor
     - external
     - public
     - internal
     - private
   - Whitespace in Expressions
     - Control Structures
   - Function Declartion Mappings
   - Variable Declaration
     - Strings
       - "Vs"
   - Operator & Space
   - Order
     - pragma
     - import
     - contract
     - types
     - state variables
     - events
     - functions

## Naming Convention

1. Types
   - lc
   - l_c
   - UC
   - U_C
   - CW
   - CW
   - Avoid
     - l (lowercase l)
     - i (lowercase i)
     - o (lowercase o)
     - Confused with 1 & 0
   - Contract
     - CW
   - Struct
     - CW
   - Event
     - CW
   - Function
     - mC
   - Function Arg
     - mC
   - Local/State Variables
     - mC
   - Constant
     - U_C
   - Modifier
     - mC
   - Enum
     - CW
   - Collision
     - built-ins
   - Security
     - Readability
     - Maintainability

# Secureum - Solidity 201

## Inheritance

1. OOP

   - Multiple Inheritance
   - Polymorphism

2. Base

   - Derived Single Contract

3. Function Override

   - virtual keyword in base
   - override keyword in derived

4. Diamond Problem
   - C3 Linearization

## Contract Types

1. Contract

2. Abstract
   - Unimplemented function within contract
     - must contain atleast one
3. Interface

   - No function can be implemented
   - All functions must be external
   - No State Variables
   - No Constructor
   - No Inheritance

4. Library
   - Deployed Once
   - Callers call library using DELEGATECALL Op code

## Using for

1. Directive

   - Ex
     - Using A for B
       - A: specifies library
       - B: specifies type
     - Attach Functions
       - Library A
         - Type B

2. Object

   - First Parameter
   - Object
     - First Parameter
   - Only inside contract

3. E.g.
   - Using SafeMath for uint256

## Base Class Functions

1. Inheritance Hierarchy

2. Derived

   - Base

3. Explicit

   - Contract.function()

4. One Level Up
   - super.function()

## Shadowing

1. State Variable Shadowing

2. Base

   - State Variable X

3. Derived X

   - State Variable X

4. Derived

   - Any Base
   - No Visible State Variables

5. Shadowing
   - Errors

## Overriding changes

1. Function Overriding

   - virtual
   - override

2. Visibility
   - external
     - public
   - non-payable
     - view
     - pure
   - view
     - pure
   - payable
     - cannot be changed when overriding

## Virutal Functions

1. Virtual Function Rules

2. No Implementation

   - virtual

3. Interface

   - All functions considered

4. Private Visibility
   - Cannot be virtual

## State Variables

1. Public state variables

2. Automatic Getters

3. External Functions

   - Params & Return Types

4. Getters
   - Override external functions
   - State Variables cannot be overridden by function

## Function Modifiers

1. Modifier Overriding

2. Overriding Possible

   - Similar to Functions

3. Overridden Modifier

   - virtual Keyword

4. Overriding Modifier
   - override Keyword

## Base Construcutor

1. Base

   - Derived Constructors

2. Constructors Called

   - Linearization Rules

3. Constructor Arguments

4. Inheritance List
   - Derived Constructor

## Name Collision

1. Pairs

   - Same Name
   - Inheritance
     - Errors

2. Function & Modifier

3. Function & Event

4. Event & Modifier

## Library Restrictions

1. No State Variables

2. Cannot

   - Cannot Inherit or be Inherited
   - Cannot Receive Ether
   - Cannot Be Destroyed

3. Calling Contract

   - Only if state variables are supplied

4. Directly vs DELEGATECALL
   - pure or view functions
   - Libraries are assumed to be stateless by default

## EVM Storage

1. Storage

   - Key/Value Store

2. Key

   - Value

3. 256-bit

   - 256-bit

4. Storage Access

   - SLOAD & SSTORE

5. Storage Location
   - Initialized to zero

## Storage Layout

1. Storage Variables

   - Storage Slots

2. Multiple Vars
   - Compact
     - Same Slot
3. State Var Order

   - Stored Contiguously

4. Exceptions
   - Dynamic Arrays
   - Mappings

## Storage Packing

1. State Variables
   - Type
     - Size in Bytes
   - Contiguous & Size Fits
     - Stored in same storage slot
   - Contiguous & Not Fit
     - Next Storage Slot
   - First Item
     - Lower-order Aligned

## Structs & Array

1. Structs & Arrays

   - Storage Rules

2. Structs & Arrays

   - Start New Storage Slot

3. Following Items

   - Start New Storage Slot

4. Elements
   - Contiguous Indivual Values

## Inheritance

1. Contract Inheritance

   - Storage Layout

2. Base(s)

   - Derived
   - State Variables Layout

3. C3-Linearized Order

   - Most Base-ward
     - Derived

4. State Variables

   - Different Contracts

5. Rules
   - Same Storage Slot

## Layout & Types

1. Reduced-size Types

   - Combined slot

2. Combine Multiple Reads/Writes

   - Same Operation

3. Multi-value Storage Slot

4. Values
   - Some Vs All
   - Read + Combine + Write

## Layout & Ordering

1. State Variables Ordering

   - Declaration
     - Packing

2. Packing

   - Gas Costs
   - SLOADS & SSTORES

3. Example
   - uint128,uint128,uint256
     - Two storage slots
   - uint128,uint256,uint128
     - Three storage slots

## Mappings & Dynamic Arrays

1. Storage Layout Unpredictable Size

2. Cannot be Stored In-Between Others

3. Occupy

   - 32 Bytes

4. Elements
   - Elsewhere
   - Starting Keccak256 hash

## Dynamic Arrays

1. Array

   - Slot P
   - Stores
     - Number Array Elements

2. Elements

   - keccak256(p)

3. Stored Contiguosly

   - Shared slots if possible

4. Dynamic Arrays
   - Dynamic Arrays
   - Recursively Apply

## Mappings

1. Mapping

   - slot p
   - stores nothing

2. Mappign[key k]

   - keccak256(h(k).p)

3. Concatenation

   - Concatenate h(k) and slot number p
   - h
     - Type-specific Function

4. Value

   - Padded 32B

5. string/byte
   - keccak256

## Bytes & String

1. Storage Layout

   - Similar to Arrays

2. Short Values
   - Length + Elements
     - Same Slot
   - Less than or Equal to 31B
     - Length\*2
   - More than or Equal to 32B
     - Lenght\*2 +1
3. Lowest Bit

   - 0 or 1

4. Array Type
   - Short or Long

## Memory

1. EVM Memory

   - Linear Layout

2. Addressed

   - Byte Level

3. Operations

   - MLOAD
   - MSTORE
   - MSTORE8
     - Store a single byte from stack to memory

4. Zero Initialized

## Memory Layout

1. New Memory Objects Free Pointer

2. Memory

   - Never Freed

3. Free Memory Pointer

   - Initially 0x80

4. Security
   - Memory Manipulations in assembly

## Reserved Memory

1. Solidity

   - 4 32B Slots

2. 0x00-0x3F(64B)
   - Hashing
     - Scratch Space
3. 0x40-0x5F(32B)

   - Free Memory Pointer

4. 0x60-0x7F(32B)
   - Zero Slot

## Memory Arrays

1. Elements

   - 32B Multiples

2. Even byte[]

   - Not bytes & string

3. Multi-Dimensional

   - pointers
     - arrays

4. Dynamic Arrays
   - Length + Elements

## Free Memory Pointer

1. Position 0x40

2. Initial Value

   - 0x80
   - Beyond reserves slots

3. Pointer points to

   - Allocatable memory

4. Memory Allocation
   - Update Free Memory Pointer

## Zeroed Memory

1. Memory Not Used

   - No Guarantee

2. Zeroed Contents

   - Cannot Assume

3. Release/Free Memory

   - No Built-In Mechanism

4. Security
   - Memory Manipulations in Solidity

## Reserved Keywords

1. Keywords

   - Reserved for Future use

2. Current Syntax

   - No
   - Future Syntax
     - Maybe

3. E.g.

   - after
   - alias
   - apply
   - auto
   - case
   - null
   - etc

4. E.g.
   - unchecked in v0.8.0

## Inline Assembly

1. Access EVM

   - Low-level Features

2. Bypasses Safety Features

   - E.g.
     - Type safety

3. Language

   - Yul

4. Assembly Block
   - assembly
     - {...}

## Assembly Access

1. External Variables

   - Functions & Variables

2. Local Variables

   - Value Type
   - Value Vs Addr

3. Storage Variables

   - Slots
   - _.slot & _.offset

4. Assignments Possible
   - Rules & Restrictions

## Yul Syntax

1. Literals & Calls

2. Variable Declarations Assignments

3. Scoping Blocks

   - if
   - switch
   - for

4. Function Definitions

## Solc 0.6.0 Breaking

1. Version that is not backwards compatible

2. Breaking Semantic Changes

   - Existing Code Changes Behavior
   - Exponentiation Result
     - Base Type
   - Not Smallest Type
     - Both Base & Exponent

## Solc 0.6.0 Explicitness

1. Virtual

   - override

2. Array Length

   - Read-only
   - Cannot resize anymore

3. Abstract Keyword
   - Introduced abstract contracts
   - Atleast one function must not be defined
4. Libraries

   - Have to implement all functions

5. Assembly Variable Restrictions

6. State Variables Shadowing
   - Not Allowed

## Solc 0.6.0 Changes

1. External Function X

   - Address
   - Address member

2. Dynamic Storage Arrays

   - push(x)
     - returns nothing

3. Unnamed Function

   - split into to functions
     - fallback()
     - receieve()

4. fallback() Vs receive()
   - fallback can be made payable or not

## Solc 0.6.0 New Features

1. try/catch

   - Failed External Calls

2. struct/enum

   - File-level

3. Array Slices

   - calldata

4. Natspec

   - return

5. Yul

   - leave

6. payable(x)

## Solc 0.7.0 Breaking

1. Breaking Semantic Changes

2. Exponentiation & Shifts

   - Literals by Non-literals

3. Earlier

   - Type of shift/exponent

4. Now
   - uint256 or int256

## Solc 0.7.0 Changes

1. Calls

   - Gas & Value
   - Now
     - block.timestamp

2. Natspec

   - Variables

3. Gwei

   - Keyword

4. String Literals

   - Unicode

5. Function State Mutability
   - Assembly Changes

## Solc 0.7.0 Removed

1. Struct/Array

   - Mapping

2. Constructor Visibility

   - No longer needed

3. Virtual Library Functions

   - Disabled because libraries cannot be inherited from

4. Events

   - Same Name/ Params are disallowed

5. Using A for B

   - Contract X
     - Derived

6. Shift by Signed Types

   - Disallowed

7. finney/szabo/var
   - Removed

## Solc 0.8.0 Breaking

1. Checked Arithmetic

   - unchecked {...}
   - checked arithmetic by default
     - Increases gas cost by default

2. Default ABI Coder v2

3. Exponentiation

   - a**(b**c) Vs (a**b)**c

4. Revert Vs Invalid Opcodes

5. Storage Byte Arrays

   - Panic raised if memory access not in range

6. Type Byte Removed
   - Used to be alias of type 1

## Solc 0.8.0

1. Explicit Conversions

   - Now Disallowed

2. Address literals

   - address
     - Instead of address payable
     - have to be explicitly converted now

3. Function Call Options

   - Once

4. log0-log4

   - Removed

5. Enum

   - 256 is max
   - Because Enum is uint8

6. Declarations Disallowed

   - this
   - super
   - \_

7. tx.origin and msg.sender

   - now have type address

8. chainId
   - Mutability now considered view
   - no longer pure

## Zero-Address Check

1. address(0)

   - Private Key

2. Transfer Ether/Token

   - Burn

3. Access Control

   - Transactions cannot be assigned with zero address

4. Zero-address Checks
   - address parameters
   - Specially user supplied

## tx.origin

1. Ethereum Accounts

   - EOA Vs Contract

2. Tx Origin

   - Only for EOA where tx originated from

3. msg.sender == tx.origin

   - Good to check if msg.sender was contract or EOA

4. Sender
   - Contract or Not

## Arithmetic Check

1. Arithmetic Overflow or Underflow

   - Results in Wrapping

2. Balances & Accounting

   - Critical Vulnerabilies

3. Solc < 0.8.0

   - SafeMath Library

4. Solc >= 0.8.0
   - Default checks

## OpenZeppelin Libraries

1. OpenZeppelin

   - Smart Contract Libraries

2. Widely Used

   - Time-tested & Optimized

3. SafeMath Library

4. Libraries
   - Token Standards
   - Security
   - Proxy
   - Utils

## OpenZeppelin ERC20

1. ERC20 Token Standard

2. All Required Functions

   - Implements all ERC20 functions for implementation

3. Increase/Decrease Allowance

4. Extensions/Presets/Utils

## OpenZeppelin ERC20 Util SafeERC20

1. Safe

   - transfer
   - transferFrom
   - approve
   - increaseAllowance
   - decreaseAllowance

2. bool Vs revert Vs Nothing

3. safe\* Wrappers

   - Revert on Failure

4. using SafeERC20 for IERC20

## OpenZeppelin ERC20 Util Token Timelock

1. Token Holder Contract

2. Token Beneficiary

   - Timed Release

3. Token Vesting

   - Advisors
   - Team
   - Etc.

4. token, beneficiary, releaseTime
   - release()

## OpenZeppelin ERC721

1. ERC721 Token Standard NFTs

2. All Required Functions

   - AddressOf
   - OwnerOf

3. Differs with ERC20

   - Transfers
   - Approvals
   - Operators

4. Extensions
   - Presets
   - Utils

## OpenZeppelin ERC777

1. ERC777 Token Standard

   - ERC20 Improvements

2. Key Feature
   - Hooks
     - tokensToSend
     - tokensReceived
3. No Approve

   - No transferFrom
   - No Stuck tokens

4. 18 Decimals
   - Operators
     - special accounts that can transfer tokens on behalf of others
   - send()

## OpenZeppelin ERC1155

1. ERC1155 Standard Fungibility-Agnostic

2. Single Contract

   - Multiple Tokens

3. Convenient & Efficient

   - Single Tx
     - Multiple Tokens

4. balanceOfBatch()
   - safeBatchTransferFrom()

## OpenZeppelin Ownable

1. Basic Access Control
   - Contract
     - Owner
2. Default Owner

   - Contract Deployer

3. Exclusive Owner Access

   - Special Functions

4. Modifier onlyOwner
   - transferOwnership()

## OpenZeppelin AccessControl

1. Generalized RBAC

   - Role-based Access Control

2. Roles

   - Permission Set

3. onlyRole

   - Restrict Access

4. grantRole & revokeRole
   - Role
     - RoleAdmin
5. Ownable

   - Simple

6. AccessControl
   - Flexible

## OpenZeppelin Pausable

1. Guarded Launch

   - Emergency
     - Pause Smart Contract to Fix while launching
     - Remediate

2. pause() & unpause()

   - Authorized Access

3. Modifiers

   - whenPaused
   - whenNotPaused

4. Vulnerability or Exploit
   - Circuit-breaker

## OpenZeppelin ReentrancyGuard

1. Reentrancy Vulnerability

   - Unique
   - Dangerous

2. External & Untrusted

   - Calls
     - Reenter & Exploit
     - Can trigger logic multiple times

3. Modifier

   - nonReentrant
     - Cannot be reentered after making an external call

4. Prevents Reentrancy
   - Best Practice

## OpenZeppelin PullPayment

1. Payment

   - Pull Vs Push
   - Avoid Reentrancy Attacks

2. Paying Contract

   - No Calls
     - Receiver Functions

3. Receiver Account

   - Withdraws Payment

4. Prevent Reentrancy
   - Best Practice
   - Favors pull payment over push payment

## OpenZeppelin Address

1. Address-related Functions
   - isContract()
     - returns False
       - is EOA
       - is contract account within constructor
       - is address where ccontract will be created
       - address had contract but is destroyed
     - returns True
       - is Contract
   - sendValue()
     - standard transfer
       - limits to 2300 gas
       - sometimes insufficient
     - send value removes 2300 limitation
       - forwards all available gas to callee contract
       - functionCall()
       - functionCallWithValue()
       - functionStaticCall()
       - functionDelegateCall()

## OpenZeppelin Arrays

1. Array-related Functions

2. findUpperBound()

   - Params
     - Array
     - Element

3. Array

   - Sorted Ascending
   - No Repeats

4. Value
   - More than or Equal to Element
     - Index
   - None
     - Length

## OpenZeppelin Context

1. Current Execution Context

2. msg.sender & msg.data

3. Meta-transactions

   - Sender X = User

4. \_msgSender() & \_msgData()

## OpenZeppelin Counters

1. Counters

   - Increment
   - Decrement

2. Use Cases

   - Mapping Elements
   - ERC721 IDs
   - Request IDs

3. current()

   - Value

4. reset()
   - zero

## OpenZeppelin Create2

1. CREATE2 EVM Op Code

   - Easier
   - Safer
   - allow contract to programmatically create other contracts
   - Similar to a deployer contract

2. deploy(uint256 amount, bytes32 salt, bytes bytecode)

   - address becomes deterministic

3. computeAddress(bytes32 salt, a bytecodehash)

   - determine address of new contract without deploying it

4. computeAddress(bytes32 salt, bytes32 byteCodeHash, address Deployer)
   - address with deploying from a different address

## OpenZeppelin MultiCall

1. Batch Calls

   - Single External Call

2. multicall(bytes[] calldata data) external

   - bytes[]

3. Receives + Executes Function Calls

   - Batch

4. One Tx, Same Block
   - Less Overhead
     - Gas Efficient

## OpenZeppelin String

1. String Operations

2. toString(value)

   - uint256
     - ASCII String Decimal

3. toHexString(value)

   - uint256
     - ASCII String Hex

4. toHexString(value, length)
   - ASCII String Hex
   - Fixed Length

## OpenZeppelin ECDSA

1. ECDSA Signatures

2. Signature

   - (v,r,s)
   - v
     - 1B
   - r
     - 32B
   - s
     - 32B

3. recover(msgHash, signature)

   - signerAddress
   - prevents maleability

4. EVM ecrecover
   - Malleable
   - OpenZeppeling ECDSA
     - v=27/28
     - s=Lower

## OpenZeppelin MerkleProof

1. Merkle Tree Proof

2. Merkle Tree Leaf

   - Root

3. verify(proof, root, leaf)

   - returns bool

4. Proof

   - Sibling Hashes

5. Branches
   - Leaf to Root

## OpenZeppelin SignatureChecker

1. ECDSA & ERC-721 Signatures

2. ECDSA

   - EOA Signatures

3. ERC-1271

   - Allows contract signatures different from ECDSA Signatures

4. Smart Contract Wallets & Other Applications

## OpenZeppelin EIP-712

1. Hashing & Signing

   - Typed Structure Data

2. EIP-712 Domain Separator

3. block.chainID & address(this)

4. Prevent Replay Attacks

## OpenZeppelin Escrow

1. Escrow Funds for Payee

   - Ownable

2. depositsOf(payee)

   - uint256

3. deposit(payee)

   - onlyOwner

4. withdraw(payee)
   - onlyOwner

## OpenZeppelin ConditionalEscrow

1. Escrow Funds for Payee

   - Conditional Withdraw

2. withdrawalAllowed()

   - Check Condition

3. withdraw(payee)

   - public Vs onlyOwner

4. require(withdrawalAllowed(payee))
   - withdraw

## OpenZeppelin RefundEscrow

1. Escrow

   - Beneficiary
   - Multiple Depositors

2. State

   - Active
   - Refunding
   - Closed

3. Active

   - Deposits

4. Refunding

   - Refunds

5. Closed
   - Beneficiary Withdrawals

## OpenZeppelin ERC-165

1. Contract

   - Interface Determine Support

2. Runtime Detection

   - Lookup Table

3. Register Interface

   - \_registerInterface(bytes4)

4. supportsInterface(bytes4 interfaceId)
   - bool

## OpenZeppelin Math

1. Math Utilities

   - Missing in Solidity

2. max(uint256 a, uint256 b)

3. min(uint256 a, uint256 b)

4. average(uint256 a, uint256 b)

## OpenZeppelin SafeMath

1. Math Functions

   - Safe
     - Overflow/Underflow

2. add & sub & mul & div & mod

3. using SafeMath for uint256

4. try\*
   - Flag Vs Revert
   - Required
     - solc < 0.8.0

## OpenZeppelin SignedSafeMath

1. Math Functions

   - Safe
     - Overflow/Underflow

2. add & sub & mul & div

3. using SignedSafeMath for int256

4. Required
   - solc < 0.8.0

## OpenZeppelin SafeCast

1. Downcasting
   - Overflow
   - Safe DownCasting
     - cast into smaller type
2. Example
   - uint256
     - uint224
     - uint128

## OpenZeppelin EnumerableMap

1. Mapping

   - Enumerable

2. Added/Removed/Checked

   - O(1)

3. Enumerated

   - O(n)

4. Supported Mapping Type
   - uint256 => address

## OpenZeppelin EnumeratedSet

1. Mapping Sets

2. Added/Removed/Checked

   - O(1)

3. Enumerated

   - O(n)

4. Supported Set Types
   - bytes
   - address
   - uint256

## OpenZeppelin BitMaps

1. Managing BitMaps

   - uint256
     - bool

2. get(bitMap, index)

   - bool

3. setTo(bitmap, index, value)
   - set(bitmap, index)
4. unset(bitmap, index)

## OpenZeppelin PaymentSplitter

1. Split Ether Payments

   - Group of Accounts

2. Sender Agnostic
   - Split
     - Equal
     - Arbitrary
3. Account

   - Shares

4. Claim

   - Proportional

5. Pull Payment Method

## OpenZeppelin TimelockController

1. Enforces Timelock onlyOwner Operations

2. Users

   - Exit

3. Operations
   - Apply
   - Schedule
   - Delay
   - Execute
   - Cancel
   - Batch
   - Pending
   - Ready
   - Done
   - updateDelays

## OpenZeppelin ERC2771Context

1. ERC-2771

   - Meta-transactions

2. Authorized

   - Tx Signer

3. Relayer

   - Gas Pay

4. Tx Signer

   - Sends to Gas Relay

5. Gas Relay

   - Sends to Trusted Forwarder

6. Trusted Forwarder
   - Contract
7. Contract
   - ERC-2771

## OpenZeppelin MinimalForwarder

1. ERC-2771

   - Meta-transactions

2. Simple Minimal Forwarder

3. Nonce & Signature Checks

4. verify(req, signature)

5. execute(req, signature)

## OpenZeppelin Proxy

1. Proxy

   - Implementation
   - Forwards via DELEGATECALL

2. \_fallback()

   - forwards call to implementation
   - \_implementation()

3. \_delegate(address implementation)

   - Allows one to specify delegation to a specific implementation contract

4. \_beforeFallback()
   - Hook
     - Delegate

## OpenZeppelin ERC1967Proxy

1. Upgradeable Proxy

   - Implementation
     - Changed

2. Data(Proxy)

   - Logic(Implementation)
   - Storage Conflict can Occur

3. constructor(address \_logic, bytes \_data)

4. \_upgradeTo(address newImplementation)

## OpenZeppelin TranparentUpgradeableProxy

1. Upgradeable

   - Admin

2. Selector Clash

   - Attack

3. Non-Admin

   - Implementation

4. Even Calls

   - Match Proxy

5. Calls X

   - Not forwarded to implementation

6. Admin

   - Admin Actions

7. Upgrade
   - Implementation or Admin

## OpenZeppelin ProxyAdmin

1. Admin Contract
   - TransparentUpgradeableProxy
2. getProxyImplementation()

3. getProxyAdmin()

4. changeProxyAdmin()

5. upgrade(proxy, implementation)

6. upgradeAndCall(proxy, implementation,data)

## OpenZeppelin BeaconProxy

1. Implementation Address

   - Upgradeable Beacon

2. Beacon Address

   - Slot
   - uint256(keccak256(eip1967.proxy.beacon))-1

3. constructor()

   - Beacon Init

4. \_beacon()

   - Beacon Address

5. \_implementation()

6. \_setBeacon(beacon, data)

## OpenZeppelin Upgradeable Beacon

1. Upgradeable Beacon

   - BeaconProxy

2. Owner

   - Change Implementation

3. Constructor

   - Implementation Init

4. Deployer

   - Owner

5. \_implementation()

6. \_upgradeTo(newImplementation)

## OpenZeppelin Clones

1. EIP-1167

   - Minimal Proxy Contracts

2. Delegate

   - Fixed Implementation

3. Deploy

   - Create
   - Create2

4. clone(implementation)

   - instance

5. cloneDeterministic(implementation, salt)
   - instance

## OpenZeppelin Initializable

1. Proxy

   - Forwards all calls to an implementation contract
     - implements logic
   - Proxy maintains state and data

2. Constructor

   - Initialize

3. All Contracts

   - Inheritance

4. Once & Immediate

   - Should be run as soon as conrtract is deployed

5. Initializer Modifier
   - Immediate
     - Deployment

## Dappsys DSProxy

1. Proxy

   - Implementation

2. Contract Bytecode

3. Function Calldata

4. Create + DelegateCall

5. DSProxyFactory & DSProxyCache

## Dappsys DSMath

1. Arithmetic Function X

   - Overflow
   - Underflow

2. add, sub, mul, min, max

   - Fixed-point math

3. Wad

   - 18 Decimals
   - wmul, wdiv

4. Ray
   - 27 Decimals
   - rmul, rdiv, rpow

## Dappsys DSAuth

1. Authorization

2. auth Modifier

   - isAuthorized()

3. msg.sender
   - Owner
   - Contract
   - authority

## Dappsys DSGuard

1. ACL

   - srcAddr, dstAddr
     - Functions Signature

2. DSAuth authority
   - canCall()
     - bool
3. [src][dst][sig]

   - returns bool

4. src

   - msg.sender

5. dst

   - Contract that includes library

6. Sig
   - Function Signature

## Dappsys DSRoles

1. RBAC (roll-based access control)

   - ACLs
     - Roles
     - Capabilities

2. canCall()

   - bool
   - User
     - Function @ Address

3. Root Users

   - Public Capabilities

4. Role Capabilities
   - Not root
   - Not public

## WETH

1. Wrapper Ether

   - Ether Vs ERC-20
   - Allows Smart Contracts to Ether sent to Contract to its ERC-20 equivalent

2. Wrapping

   - To ERC-20

3. Unwrapping
   - Ether
4. WETH Contract

   - 1:1

5. WETH9
   - 7M Ether
6. WETH10

   - Efficiency
   - EIP-3156 Flash Loans

## UniSwap V2

1. AMM (Automatic Market Maker)

   - x\*y=k
     - x,y : token balances
     - k : constant product

2. Pools, Token Pair

   - LP & LP Tokens

3. Swaps

   - Token Pair
   - Maintain x\*y=k

4. Oracles
   - TWAPs
     - Time Weighted Average Prices
   - Measures price at the beginning of each block

## Uniswap V3

1. Concentrated Liquidity

   - Custom Price Ranges

2. Capital Efficiency

3. Flexible Fees

   - 0.05%, 0.30% and 1.00%

4. Advanced TWAP
   - Cumulative Sums
     - One
       - Array

## Chainlink

1. Oracles & PriceFeeds

2. Offchain Data Providers

   - Onchain Feeds

3. Oracles

   - Chainlink N/W
   - Aggregated Data

4. AggregatorV3Interface

# Security Pitfalls & Best Practices 101

## Solidity

1. Old Vs New Versions

   - Breaking changes introduced roughly every year

2. Old

   - Bugs
   - Time-Tested
   - Less Features

3. New
   - Bug-fixes
   - New Bugs
   - Mor Features
4. Optimal Version
   - Security Vs Functionality

## Unlocked Pragma

1. Solidity Pragma

2. Use of ^

   - Unlocked
   - If ^ symbol is used pragma is considered unlocked
   - Any compiler version within the breaking version can compile Smart Contract

3. Testing Vs Deployment

   - Different Versions
   - Risky from a Security Perspective

4. Lock Pragma
   - Test
   - Deploy

## Multiple Pragma

1. Solidity Pragma

   - Different Pragmas
   - Different Contracts

2. Different Bugs

   - Different Features
   - Different Checks

3. Same Pragma
   - Same Bugs
   - Same Features
   - Same Checks

## Access Control

1. Access to Functions

2. Public/External Functions

3. Addresses
   - Anyone
   - Owner
   - RBAC
4. Correct Modifiers/Address
   - Enforce Access

## Withdraw Funds

1. Unprotected Withdraw Functions

2. Public/External Withdraw ETH/Tokens

3. Unauthorized Withdraws

   - Loss of Funds

4. Access Control
   - Withdraw Functions

## Selfdestruct

1. selfdestruct()

   - unprotected selfdestruct can cause User to destroy contract

2. Unauthorized Call

   - Contract Killed

3. Access Control
   - Authorized Users

## Modifiers Side-effects

1. Modifier Side-effects

2. Modifier

   - Checks
   - No Side-effects

3. Unnoticed Side-effects

   - Readability
   - Auditability

4. Security
   - Modifiers should not have side-effect
   - Only Checks

## Incorrect Modifier

1. Incorrect Modifier

   - Checks
   - Execute \_ or Revert

2. Default Value Returned

   - Unexpected

3. All Modifier Paths
   - Execute \_ or Revert

## Constructor Names

1. < 0.4.22

   - Contract Name as constructor

2. < 0.5.0

   - Contract Name or constructor
   - Caused security issue if both existed

3. > = 0.5.0

   - Only constructor

4. Naming Confusion
   - bugs

## Void Constructor

1. Base Constructor

2. Calling Unimplemented Constructors

3. Misplaced Assumptions

4. Check Implementation
   - Call or Not

## Constructor callValue

1. Implicit Constructor

   - callValue Check

2. Not Explicitly Payable

   - Constructor
     - Revert

3. Base Constructor

   - !=0 callValue
     - No Revert

4. Compiler Bug
   - Bug present from v0.4.5 - v0.6.8

## delegateCall

1. Controlled delegateCall

2. User-controlled Address

3. Malicious Contracts

4. Contract State

   - Unauthorized Modification

5. delegateCall
   - Should only be allowed to be used by trusted addresses

## Reentrancy

1. External Contract Calls

   - Reentrancy

2. Contract Callbacks

   - C1 -> C2 -> C1

3. Multiple Withdrawals

4. OOO (Out of Order)Events

5. CEI Pattern
   - Checks Effects Interactions Patterns
   - Effects
     - Changes to the state of the calling contract
   - Interactions
     - Use interactions with external contracts last
6. Reentrancy Guard

## ERC777

1. ERC777 Token Standard

   - Callbacks
     - Reentrancy

2. ERC20 Extension

   - Token Transfer
     - Hooks

3. Hooks

   - Reentrancy
   - C1 -> ERC777 -> Hook -> C1

4. CEI Pattern
   - Checks Effects Interactions Patterns
   - Effects
     - Changes to the state of the calling contract
   - Interactions
     - Use interactions with external contracts last
5. Reentrancy Guard

## transfer() & send()

1. ETH transfer() & send()

2. ETH tranfer() & send()

   - Reentrancy Mitigations

3. Gas Subsidy 2300
   - Reentrancy
     - No Gas
4. OpCode Gas Repricing

   - Break Contracts

5. Security Implementations
   - call()
     - Use lo
   - CEI Pattern
   - Reentrancy Guards

## Private Data

1. Privacy of On-Chain Data

2. private Variables != Cannot read

3. Blockchain Transactions & State On-Chain Vs Off-chain

4. Private Data
   - Encrypted & stored off-chain

## PRNG (Pseudo Random Number Generation)

1. PRNG in Contracts
   - Randomness Applications
2. block.timestamp
   - blockhash
3. High Stakes
   - Miner Influence

## Risk Awareness

1. Alternatives
   - VRF
     - Verifiable Random Function

## Time

1. On-chain Time

2. block.timestamp

3. block.number

4. Miner Influence

5. Synchronization

6. Unpredictable

7. Risk Awareness
   - Alternatives
     - Oracles

## Overflow/Underflow

1. Integer Arithmetic

   - Overflow
   - Underflow

2. Wrapped Values

   - Invalid

3. Data

   - High/Low

4. Unexpected Behavior & Vulnerabilities

5. Prevention
   - Use OpenZeppelin SafeMath
   - Default Checks
     - Using solc versions >= 0.8.0

## Divide Before Multiply

1. Integer Arithmetic

   - Divide before Multiply

2. Solidity Integer Division

   - Truncation

3. Division

   - Multiplication
   - Loss of Precission

4. Prevention
   - Multiplication before Division

## TOD (Transaction Order Dependence)

1. Mempool Transactions

   - Transaction Inclusion

2. Front-running

3. Back-running

4. Do Not Make Assumptions
   - Transaction Order

## ERC20 approve()

1. ERC20 approve()
   - Race-condition
2. approve(100)
   - approve(50)
3. Allowance Decrease
   - Front-run to spend 150
     - Gives spender allowance of 50
     - And allows spender to remove 150
4. Prevention
   - increaseAllowance()
   - decreaseAllowance()

## ecrecover

1. EVM ecrecover

   - Signature Malleability

2. Signature

   - Components
     - v
     - r
     - s
   - Check s
     - Lower Range

3. Can Result

   - In replay attacks

4. Prevention
   - Use OpenZeppelin ECDSA library

## transfer()

1. ERC20 transfer()

2. Specification

   - Boolean Return Value

3. No Return Value

   - Revert solc >= 0.4.22

4. Prevention
   - OpenZeppelin SafeERC20 Wrappers

## ownerOf()

1. ERC721 ownerOf()

2. Specification

   - Address
   - Return value

3. Bool Return Value

   - Revert
   - Was ok until solc >= 0.4.22
     - Now causes Revert

4. Prevention
   - Use OpenZeppelin SafeERC20 Wrappers

## Contract Balance

1. Unexpected Ether

2. Creation

   - Payable Functions

3. Coinbase Tx

4. selfdestruct()

5. Assumptions on this.balance
   - Can become invalid based on extreme assumptions

## fallback() vs receive()

1. Differences and Similarities

   - Visibility
   - Mutability
   - Ether Transfers

2. Prevention
   - Check Assumptions & Implications

## Strict Equalities

1. Strict Equalities

   - Dangerous

2. == Vs <= or >=

3. ETH/Token

   - Transfer & Balances

4. Check Constraints
   - Safe Defaults

## Locked Ether

1. Contract Balance

   - Locked Ether

2. Payable Functions

   - No Withdraw

3. Can Deposit

   - Cannot Withdraw

4. Remove Payable

5. Add withdraw

## tx.origin

1. Use of tx.origin

   - Considered Dangerous in certain situations

2. tx.origin

   - Ethereum Owned Account

3. Authorization

   - MITM Replay Attack
     - Man In the Middle (MITM)
       - Attacker comes in between user and contract and replays transaction

4. Prevention
   - Use msg.sender instead of tx.origin

## Contract

1. Contract Vs EOA

2. extcodesize > 0

3. msg.sender == tx.origin

   - tx.origin can only be an EOA

4. Pros & Cons

   - Based on Applications

5. Risk Awareness
   - Implications

## delete Mapping

1. delete mapping within struct

   - delete struct fields
   - leaves mapping intact

2. Unintended consequences

3. Use Alternatives
   - Lock Vs Delete

## Tautology Contradiction

1. Tautology

   - Always true

2. Contradiction

   - Always false

3. x >= 0

   - uint x

4. Security Concerns
   - Flawed logic
   - Redundant Checks

## Boolean Constant

1. Boolean Constants

   - true or false

2. Use in Conditionals

   - Unnecessary

3. Security Concerns
   - Flawed logic
   - Redundant Checks
   - To Avoid
     - Remove checks or Simplify logic

## Boolean Equality

1. Boolean Equality

   - true or false

2. Use in Conditionals

   - if(x==true)

3. Security Concerns

   - Redundant Use
   - Unnecessary
   - To Avoid
     - if(x) instead of if(x==true)

## State Modification

1. Contract State Modifications

2. Functions

   - view
   - pure

3. solc >= 0.8.0
   - STATICCALL
     - Revert
     - STATICCALL is called with view or pure functions
4. Function Mutability
   - Check & Apply

## Return Values

1. Function Return Values

   - Low-level calls
     - call
     - delegateCall
     - send

2. Check Return Value
   - Success/Failure

## Unexpected Failure

1. Account Existence
   - Low-level calls
     - call
     - delegateCall
     - send
2. No Account

   - Return true

3. Check Existence Before Call

## Shadowing

1. Solidity Built-in

   - Shadowing

2. Built-in

   - now
   - assert, etc.

3. Names

   - Variables
   - Functions
   - Modifiers

4. Override Behavior

   - Dangerous
   - Unexpected

5. State Variables Shadowing
   - Contracts
     - Base Vs Derived
   - Confusion with variable names
     - Base Variables
     - Shadowed Variables
   - Wrong Variable Usage
     - Dangerous
     - Unexpected
     - Shadowing of state variables is now disallowed

## Pre-Declaration

1. Local Variables

   - Pre-declaration Usage

2. Declared Later

3. Declared Another Scope

4. solc < 0.8.0

5. solc >= 0.8.0
   - C99-style Scoping Rules

## Costly Operations

1. Costly Operations Inside Loops

2. State Variable Updates

3. Out-of-Gas Error

4. Use Local Variables
   - To Prevent DoS use local variables instead of state variables

## Costly Calls

1. External Calls Inside Loops

2. Loop Index

   - User Controlled

3. Reverts

   - Out-of-Gas Error

4. Avoid Calls in Loops
   - Prevent DoS

## Block Gas Limit

1. Block Gas Limit

   - 15M Currently

2. Loop Index

   - User Controlled

3. Expensive Operations

   - Out-of-Gas Error

4. Evaluate Loops
   - Prevent DoS

## Events

1. Missing Events

   - Critical Operations

2. Off-Chain Monitoring

3. Transperency & UX

4. Add Events
   - Critical Operations

## Event Parameters

1. Event Parameters

   - Not Indexed

2. Indexed

   - Topics
     - Accessed or queried faster

3. Not Indexed
   - Data
     - Accessed or queried slower

## ERC20 Specification

1. Faster Lookup

2. Add 'Indexed'

   - Critical Parameters

## Event Signatures

1. Event Signatures

   - Contract Type

2. Contract Parameter
   -Address Vs Name

3. Wrong Hash
   - solc Bug
     - 0.5.0
     - 0.5.8
       - Compiler bug
       - Address Type was used instead of contract name

## Unary Expression

1. Unary Expressions

   - Typo Susceptibility
   - x += 1
     - Increment
   - x =+ 1
     - Re-initialize

2. Unary + Deprecated
   - solc 0.5.0

## Zero Address

1. Zero Addresses

   - Special Consideration

2. Defalt Value

   - Also Known as Burn Address

3. Tokens Burnt

   - Contract Locked

4. Best Practice
   - Zero-address Checks on all address parameters

## Critical Addresses

1. Critical Addresses

   - Change Value

2. Single-step Change

   - Prone to Error
     - If incorrect address used is contract locked

3. Two-step Change

   - Grant/Approve + Claim

4. Error Recovery

   - Risk Mitigation

## assert()

1. Use of assert()

2. Assert Invariants

   - Used only to check or verify program invariants

3. No State Change

4. Not Validate Inputs

   - Use require instead

5. Best Practice
   - No assert() should expect failure
   - Normal Contract Function

## assert Vs require

1. assert() Vs require()

2. assert()
   - Used to check or verify invariants
     - We do not expect assert() to fail
3. require()

   - Used for input validation
     - Failures Expected

4. Best Practice

   - Use Appropriately

5. Previously
   - Before solc 0.8.0
     - assert() used INVALID Op Code
     - require() used REVERT Op Code
     - This resulted in different gas usage

## Keywords

1. Deprecated Keywords

2. E.g.

   - msg.gas
     - Mainly use msg.gasLeft now
   - throw
     - Mainly use revert now
   - sha3
     - Mainly use keccak256
   - constant
     - Mainly use view
   - var
     - Strongly typed is preffered now
   - Etc.

3. Best Practice
   - Avoid Deprecated Keywords

## Visibility

1. Functions

   - public
   - external
   - internal
   - private

2. solc < 0.8.0

   - Default
     - public
   - This allowed users to access functions that did not have visibility assigned

3. Unauthorized Access

   - Removed
     - solc 0.5.0

4. Explicit Function Visibility

## Inheritance Order

1. Inheritance Order

2. Multiple Contracts

   - Identical Function

3. Order

   - Implementation

4. More General -> More Specific

## Inheritance Missing

1. Missing Inheritance

   - Appears to inherit from abstract contract, interface, etc.

2. Appear

   - Interface
   - Abstract Contract

3. Inherit Appropriately

4. Best Practice
   - Specify Inheritance
   - Avoid naming contracts too similarly

## Gas Griefing

1. Transaction Relayers

2. Users

   - Forward Tx to the blockchain with the correct amount of Gas

3. Tx

   - Sufficient Gas
   - Success/Fail

4. Best Practice
   - Trust in Relayers

## Reference Parameters

1. Function Parameters

   - Reference Types

2. Pass by Value or Pass by Reference

3. Structs/Arrays/Mappings

   - Memory Vs Storage

4. Unexpected Changes
   - Aware
     - Value/Reference

## Arbitrary Jump

1. Function Type

   - Arbitrary Jump

2. Variable Assignment

   - Assembly Code

3. Function Variable

   - Arbitrary Code

4. Avoid assembly
   - Arbitrary Function Values

## Hash Collisions

1. abi.encodePacked()

   - variable length arguments

2. No zero-padding

3. No length

4. Packed Encoding

   - Collisions Possible

5. Best Practice
   - Avoid encodePacked()
     - Use abi.encode()
   - Or only one variable length argument used with abi.encodePacked()
   - No Dynamic to taint the value which can force collisions

## Dirty Bits

1. Types < 32 Bytes

2. Dirty High Order Bits

   - Contain values to those previous bits

3. Type Operations

   - Ok

4. msg.data

   - Not Ok

5. Risk Awareness

6. Best Practice
   - Zero out unused bits

## Incorrect Shifts

1. Shift Operators

   - shl(x,y)
   - shr(x,y)
   - sar(x,y)

2. Shift y by x bits

3. Confusing

   - Exchanged Check Shifts

4. Best Practices
   - Ensure developer has correct idea of shifting

## Assembly

1. Solidity Assembly

2. Optimized

   - Efficient Gas Savings

3. Error-Prone

   - Semantics & Readability

4. Best Practice
   - Avoid as much as possible
   - Double-check that op codes are used correctly

## RTLO(Right-to-Left-Override)

1. RTLO

   - Renders text from right to left instead of the usual left to right

2. Unicode U+202E

3. RTL Text Rendering

   - Trick Users/Auditors

4. Best Practice
   - Ensure Absence of RTLO

## Constant

1. Constant State Variables

2. Declare Constant Save Gas

3. Compile-time
   - Replaces state variables with a constant
4. Replacement

   - No SLOADs

5. Identify & Declare

## Variables Names

1. Variable Names

2. Similar

   - Confusing

3. Replaced Usages

4. Readability

5. Best Practices

   - Distinct Names
   - Avoid Errors

## Variables Uninitialized

1. Unitialized State/Local Variables

2. Default Values
   - Value
     - Zero
   - Boolean
     - False
   - Address
     - Zero Address
3. Best Practice
   - Initialize Variables
   - Avoid Errors

## Storage Pointers

1. Uninitialized Storage Pointers

2. Local Storage Pointers

   - Uninitialized
     - Can point to unexpected storage locations

3. Best Practice
   - Error-prone
     - solc >= 0.5.0 Disallowed

## Function Pointers

1. Uninitialized Function Pointers

2. Constructors

   - Unexpected Behavior when used within constructors

3. Bug Present

   - solc 0.4.5 - 0.4.26
   - solc 0.5.0 - 0.5.7

4. Compiler Bug
   - Fixed

## Number Literals

1. Long Number Literals

2. Too Many Digits

   - Error-prone
   - E.g.
     - uint 1_ether = 10000000000000000000000

3. Best Practice
   - Use Ether/Time Suffix
   - Use Scientific Notation

## Enum

1. Out-of-range Enums

2. enum E[a]

   - E(1)
     - Out-of-range

3. Compiler Bug

   - solc < 0.4.5
   - Compiler Bug is now fixed

4. Best Practice
   - Check Enums

## Public Functions

1. Function Visibility

   - Public Vs External

2. Public

   - Consume more gas than external functions
   - Arguments of public functions need by copied from calldata to memory
     - This results in more op codes which results in more gas

3. Function
   - Functions that are not called within the contract should be declared external

## Dead Code

1. Contract Code

   - Dead or Unreachable

2. Programmer Error

3. Missing Logic

4. Optimization

   - Without optimization
   - Code Size increases
   - Deploy Cost increases

5. Dead Code Effects

- Scenario 1 - Unrealized dead code
  - Reduce security by tesing dead code without realizing it is never used
- Scenario 2 - Dead Code is Found and left in contract
  - Reduce security by leaving code that can introduce vulnerabilities without money
- Scenario 3 - Wrongfully identified dead code
  - Reduce security by identifying and removing wrongfully identified dead code that is part of the logic

6. Best Practice
   - Use Dead Code
     - Add logic to use code
   - Remove Dead Code

## Return Value

1. Function Return Values

   - Return values with computations of function logic

2. Call Sites

   - Unused

3. Missed Error Checking

4. Unexpected Behavior

5. Return Values
   - Check or Remove

## Variables Unused

1. State/Local Variables

   - Declared & Unused

2. Error

   - Missing Logic
   - Optimization

3. Best Practice
   - Utilize variables within logic
   - Remove unused variables

## Statements

1. Function Statements

2. Present & No Effects

3. Error

   - Missing Logic
   - Optimization

4. Best Practice
   - Evaluate if statements are redundant
     - Should statements have side effects, if not then remove

## Storage Array (Compiler Bug)

1. Storage Array

   - Signed integers

2. ABIEncodeV2

   - Type[] = int[]

3. Assignment

   - Data corruption

4. Compiler Bug
   - Fixed
   - Present: solc 0.4.7 - 0.5.10

## Constructor Arguments (Compiler Bug)

1. Constructor Dynamic Arguments

2. ABIEncoderV2

   - Dynamic Arrays

3. Revert or Invalid Decode

4. Compiler Bug
   - Fixed
   - Present: solc 0.4.16 - 0.5.9

## Arrays (Compiler Bug)

1. Storage Arrays

2. ABIEncoderV2

   - Structs or Static Arrays

3. Invalid Encode

   - External function
   - abi.encode()

4. Compiler Bug
   - Fixed
   - Present: 0.4.16 - 0.5.10

## Structs (Compiler Bug)

1. Calldata Structs

2. ABIEncoderV2

   - Static & Dynamic Encode

3. Read

   - Incorrect Values

4. Compiler Bug
   - Fixed
   - Present: solc 0.5.6 - 0.5.11

## Storage (Compiler Bug)

1. Packed Storage

2. ABIEncoderV2
   - Structs/Arrays
     - Type < 32B
     - Could cause data corruption when struct param is less than 32B
3. Storage Encode

   - Data Corruption

4. Compiler Bug
   - Fixed
   - Presetn: solc 0.5.0 - 0.5.7

## Loads (Compiler Bug)

1. Incorrect Loads With Yul Optimizer

2. ABIEncoderV2 + Yul

   - MLOAD/SLOAD Calls
   - Replaced Calls with state values

3. Compiler Bug
   - Fixed
   - Present: solc 0.5.14 - 0.5.15

## Arrays (Compiler Bug)

1. Array Slices

2. ABIEncoderV2

   - Dynamically Encoded Base Types
   - Results in invalid data when read

3. Compiler Bug
   - Fixed
   - Present: solc 0.6.0 - 0.6.8

## Escaping (Compiler Bug)

1. Missed Escaping

2. ABIEncoderV2

   - String literals that contained the double backslash "\\" would result in a different string

3. Compiler Bug
   - Fixed
   - Present: solc - 0.6.8

## Shift (Compiler Bug)

1. Double Shift Size Overflow

   - Results in unexpected values being output

2. Optimizer

   - Double Bitwise Shifts if optimizer is enabled
   - If the result of the shift is more than 2\*\*256 then this results in an overflow

3. Compiler Bug
   - Fixed
   - Present: 0.5.5 - 0.5.6

## Byte Instruction (Compiler Bug)

1. byte Opcodes bug

   - If second argument is equal to 31 or a constant expression that is equal to 31
     - Results in unexpected values
   - Incorrectly Optimized

2. Occurances of Byte Instruction Bug

   - Occurs when the index is accessed on a bytes type
     - i.e. bytes1, bytes32, bytes128, ..., bytes256
   - Occurs when the byte keyword is used in assembly

3. Compiler Bug
   - Fixed
   - Present: solc 0.5.5 - 0.5.7

## Assignment (Compiler Bug)

1. Essential Assignments Removed

2. Yul Optimizer

   - The Yul Optimizer removes variables for variables declared specifically inside for loops
   - This occurs while using Yuls continue or break statements
     - Assignments are removed here

3. Compiler Bug
   - Fixed
   - Present:
     - 0.5.8 - 0.5.16
     - 0.6.0 - 0.6.1

## Private Functions (Compiler Bug)

1. Private Functions

   - Note that private functions cannot be inherited from the base contract
   - If the derived contract creates a function with the same name and type
     - This can change the behavior of the base contract's private function

2. Compiler Bug
   - Fixed
   - Present: solc 0.3.0 - 0.5.17

## Tuples (Compiler Bug)

1. Tuple Assignments

   - Tuple assignments where components occupy mulitple stack slots are occupied
     - E.g.
       - Nested Tuples
   - Results in Invalid Values

2. Compiler Bug
   - Fixed
   - Present: solc 0.1.6 - 0.6.6

## Dynamic Arrays Cleanup (Compiler Bug)

1. Dynamic Arrays
   - When dynamic arrays were assigned with types <= 16 Bytes the assigned array shrinks
     - Note some parts of the deleted slots were not deleted by the compiler
2. Compiler Bug
   - Fixed
   - Present Until: solc 0.7.3

## byte Array (Compiler Bug)

1. Empty Byte Array Copy
   - When byte Arrays were copied from memory or calldata that were empty result in data corruption
     - Note Only Occurs When:
       - Only if target Arrays length is increased without storing new data
2. Compiler Bug

   - Fixed
   - Present Until: solc 0.7.4

## Memory Array (Compiler Bug)

1. Memory Array Creation Overflow

2. Very Large Memory Arrays

   - When a very large memory array would be created it would result in overlapping memory regions
     - Results in data corruption

3. Compiler Bug
   - Fixed
   - Present: solc 0.2.0 - 0.6.5

## using for Primitive (Compiler Bug)

1. Calldata Parameters using for

   - The parameters used in the function calls were in the calldata portion of the EVM
     - Reading the parameters resulted in Invalid Data

2. Compiler Bug
   - Fixed
   - Present: solc 0.6.9 - solc 0.6.10

## Free Functions (Compiler Bug)

1. Free Functions

   - Free functions are declared from outside of the contract
   - Defining a function with the same name and same parameters resulted in no compiler error
     - This bug allowed collisions

2. Compiler Bug
   - Fixed
   - Present: solc 0.7.1 - 0.7.2

## Initializers (Proxy Based Contracts)

1. Proxy Contract

   - In a typical proxy contract there is usually a proxy contract that does a DELEGATECALL to a logic contract
   - The logic contract gets to implement logic that executes on the state of the proxy contract

2. Unprotected Initializers

   - Implementation Contracts expected to declare and initialize parameters
   - Constructors should not be used to initialize
     - Initialize() is used instead

3. Security Pitfalls

   - Multiple Invocations
     - Reinitialize the Contract with values that let them exploit the library

4. Best Practice
   - Use OpenZeppelin Initializable library
     - This library provides an Initializer Modifier

## State Variables (Proxy Based Contracts)

1. State Variables Initialized

2. State Variables

   - State variables in the implementation contract should not be initialized in the declarations themselves
   - Initializations will not be reflected when the proxy contract makes a DELEGATECALL to this implementation contract

3. Initialize
   - State variables should be initialized should be within the initialize() function

## Import Contracts (Proxy Based Contracts)

1. Imported Contracts
   - Imported contracts that the proxy-based contracts are derived from should also adhere to proxy contract standards
   - Rules
     - Base Contracts
       - Should not use constructor() instead initialize()
       - Should not initialize state variables during declaration
   - If not state could result in undefined behavior when used or could result in serious vulnerabilities

## Selfdestruct (Proxy Based Contracts)

1. selfdestruct()

   - Issue: Data proxy calls a logic implementation contract that has a selfdestruct() which will destroy contract
     - Result: All calls to the logic contract will end up delegating calls to an address that does not have any code

2. delegateCall()

   - Issue: Using delegateCall() will cause issues because the logic implementation works with the state of the data proxy

3. Best Practice
   - Avoid using selfdestruct() with proxy-based contracts
   - Avoid using delegateCall() with proxy-based contracts

## State Variables (Proxy Based Contracts)

1. State Variables

   - State Variables Order/Layout/Type/Mutability
     - Ensure that proxy contract and implementation contract have the same Order, Layout, Type, and Mutabiility
     - If not the same then this could cause storage layout mismatch errors which can cause critical errors

2. Best Practice
   - Ensure the same Order, Layout, Type, and Mutability in proxy-based setups

## Function ID (Proxy Based Contracts)

1. Function ID Collision

   - When keccak256 of function name is the same as another
   - At runtime the function dispatcher in the contract byte code determines if one of the functions in the proxy is being called or needs to be delegated to the implementation contract

2. Malicious Proxy

   - In this setup a malicious proxy contract can hijack a call by providing the same Function ID
   - This would allow them to exploit the malicious proxy which could lead to the execution of a function that exploit

3. Best Practice
   - Pay attention to the proxy and remove any trust assumptions related to proxy and implementation contracts
   - Check if the proxy has or can declare a function whose ID might collide with one of the implementation contract functions

## Shadowing (Proxy Based Contracts)

1. Function Shadowing

   - Instead of the proxy contract covertly trying to hijack calls meant for the implementation by declaring functions whose
   - Function IDs collide with the implementation contracts function the functions could just be shadowed
   - Function could have the same name and provide the same function name, types and parameter i.e. shadowing
   - Proxy Shadowing Effects
     - Function Shadow to intercept the call

2. Best Practice
   - Pay attention to the proxy and remove any trust assumptions related to proxy and implementation contracts
   - Check if the proxy has or can shadow a function implementation contract functions

# Secureum Security Pitfalls & Best Practices 201

## ERC20 Transfers (Tokens)

1. ERC20 transfer() & transferFrom()

   - Accoring to the specification these should return boolean values
     - Note: Not all tokens abide by the specifations

2. No Boolean Return

   - Callers that assume boolean value will return will fail

3. Best Practice
   - ERC20 token contracts to ensure that boolean values are returned
   - From Caller side, do not assume that boolean values will be returned
   - Preferably use OpenZeppelin ERC20 wrappers

## ERC20 Optional (Tokens)

1. ERC20

   - Makes it optional for contracts to implement name, symbol, & decimals

2. Best Practice
   - Assume the ERC20 name, symbol, & decimal parameters are not implemented and verify that they are

## ERC20 Decimals (Tokens)

1. ERC20 decimals

   - Decimals in Token Typically 18 decimals in precision
   - ERC20 Tokens that do not adhere to the standards use uint256 type for decimals
     - If the Token returns a type uint256 with a value
       - Check that the value is less than or equal to 255
       - This is because uint8.max is 255

## ERC20 approve() (Tokens)

1. ERC20 approve() Race-Condition

   - Ex
     - approve(100) increase allowance with approve(50)
     - Allowance Decrease
       - Spender maybe to observe this operation and spend 100 and then 50 which results in spending 150

2. Best Practice
   - Do not use approve() instead use increaseAllowance() and decreaseAllowance()

## ERC777 Hooks (Tokens)

1. ERC777 Hooks
   - get called before
     - send
     - transfer
     - mint
     - burn
     - operatorSend
   - Avoid having hooks make external calls
     - This could allow for Reentrancy
2. Best Practice
   - Check for Hooks and make sure no external calls are being made

## Token Deflation (Tokens)

1. ERC20 Token Defaltion

   - transfer/transferFrom
     - Results in a Token Fee
   - Number of tokens received by target address may not be the same as the number of tokens sent by sender
     - This depends on the amount of fee and if the fee is being charged at all

2. Best Practices
   - Check Deflation for unexpected behavior
   - For smart contract applications that work with ERC20 contracts should be aware of deflation
     - Make sure accounting logic acccounts for this
   - Consider guarded launch where initial set of tokens do not have notion of deflation

## Token Inflation (Tokens)

1. ERC20 Token Inflation
   - transfer/transferFrom
     - Results in more tokens, i.e. Token Interest
   - Number of tokens received by target address may not be the same as the number of tokens sent by sender
     - Results in more tokens than sender sent
2. Best Practice
   - Check Inflation for unexpected behavior
   - For smart contract applications that work with ERC20 contracts should be aware of deflation
     - Make sure accounting logic acccounts for this
   - Check for assumption that ensures that no ERC20 Tokens are being trapped in contract
   - Consider guarded launch where initial set of tokens do not have notion of inflation

## Token Complexity (Tokens)

1. ERC20 Token Contract

   - Should have a well-defined spec for a simple contract

2. Best Practice
   - Avoid complexity as it is primed for introducing bugs

## Token Functions (Tokens)

1. ERC20 Token Contract

   - Only should have token related functions
   - No/Few non-token functions
   - This is to reduce complexity
     - Complexity increases bugs

2. Best Practice
   - Avoid unnecessary complexity

## Token Address (Tokens)

1. ERC20 Token Address

   - There is a single entry-point for checking balances of users
   - Using Multiple Addresses and Multiple Balances results in multiple entry points
     - Introduces bugs
     - Specifically accounting bugs

2. Best Practice
   - Make sure that ERC20 only works with a single address

## Token Upgradeable (Tokens)

1. ERC20 Token Upgradeability

   - Upgradeability is a concern because it can be detrimental to user trust in contracts
     - This is because of functionality change
   - ERC20 Token Functions meant to be simple
     - Mint
     - Burn
     - Transfer Rules

2. Best Practice
   - Check and verify that the Token Contract is not Upgradeable

## Token Mint (Tokens)

1. ERC20 Token Minting

   - Increment the account balances of addresses to which those new tokens are credited

2. Owner

   - Be aware of owner capabilities

3. Malicious Owner

   - Infinite Minting results in security breaches because all other users will be affected due to reducing relative shares

4. Best Practice
   - Be aware of owner misuse or abuse

## Token Pause (Tokens)

1. ERC20 Token Pausing

   - An ERC20 Token Pausing is known as a guarded launch

2. Owner

   - Malicious or compromised owner could pause the contract functionality
     - Resulting in trapped funds

3. Best Practice
   - To be aware of the risk of token pausing
   - Check & Verify if the contracts are pausable or not by owners

## Token Blacklist (Tokens)

1. ERC20 Token Blacklist

2. Owner

   - Actors who are allowed to access, add, or remove addresses from blacklist

3. Blacklist Contract

   - Can trap funds if owners are compromised or malicious

4. Best Practice
   - Check if contracts can or cannot blacklist
   - Be aware of risk with blacklists

## Token Team (Tokens)

1. ERC20 Token Team

   - Can be publicly known where we know who the project members are
   - Project members are only known by there handles
     - i.e. twitter, GitHub, other Socials

2. Schools of Thought

   - Anonymous Team is Bad

     - Riskier & more reputational risk because builder history is not known
     - It is unkown if user is a learner

   - Anonymous Team is Indifferent
     - Evaluate project itself without considerations of builders

3. Best Practices
   - Team/Legal Risk
   - Risk awareness regardless of school of thought

## Token Ownership (Tokens)

1. ERC20 Token Ownership

2. Who Owns? How Much?

3. Ownership

   - Owners may be able to influence price, governance, liquidity
     - Depending on how many tokens owners own

4. Best Practice
   - Risk of centralization because major token holder can influence the protocol
   - Risk Awareness with Token Ownership

## Token Supply (Tokens)

1. ERC20 Token Supply

2. Token Supply

   - The number of ERC20 tokens that are supported by the token contract
   - Could be low or high
   - Low Supply
     - Ownership, liquidity, and Volatility could all be concentrated

3. Best Practices
   - A limitied supply increases the risk of manipulation
   - Risk Awareness

## Token Listing (Tokens)

1. ERC20 Token Listing

   - May get listed on CEXs or DEXs
   - If token is listed on few CEXs
     - If access is down or hacked volatility or liquidity could be affected
   - If token is listed on a DEX are more resilient to failures and are expected to be up and accessible

2. Best Practice
   - If tokens are listed on few exchanges then there can be a centralization risk
   - Risk Awareness

## Token Balance (Tokens)

1. ERC20 Token Balance

2. Logic
   - Contracts that assume that the balance is always below a certain threshold could risk assumptions being broken
   - Could be broken if balance exceeds those thresholds
   - Flash Loans or Whales could cause this
   - Flash Loans
     - User is allowed to borrow a significant amount of tokens without providing collateral
       - Loan is forced to be repaid within the same transaction
       - Within the transaction the flash loan could be use to arbitrage opportunities or exploit vulnerabilities
3. Best Practices
   - Be aware that in incorrect logic may be manipulated using flash loans
   - Risk Awareness

## Token Minting (Tokens)

1. ERC20 Token Flash Minting

   - Flash minting mints tokens that are handed to the user
     - Only available within the context of a transaction
       - Destroys minted tokens after context of transaction has finished

2. Assumptions
   - If the user contracts makes assumptions about the balance or supply for the user which could lead to overflow or other security vulnerabilities

## ERC 1400 Addresses (Token Standards)

1. Introduced Permissioned Addresses

   - Driven by polymath
   - Related to the concept known as security tokens

2. Permissioned Addresses

   - Could block transfers to or from certain addresses

3. DoS Risk
   - If addresses can be compromised or are malicious then a DoS can be introduceds

## ERC 1400 Transfers (Token Standards)

1.  ERC1400 Forced Transfers

2.  Trusted Actors

- Trusted actors within the notions of the standard that can perform unbounded transfers

3.  Unbounded Transfers

- Trusted actors can transfer funds to whichever actors that they choose
  - Introduces transfer risk

4. Transfer Risk
   - Be aware of the risk involved with forced transfers and how the actors may play
   - Risk Awareness

## ERC 1644 Transfers (Token Standards)

1.  ERC1644 Forced Transfers

2.  Controller Role

    - Part of ERC 1400
    - Can perform aribtrary transfer of funds to arbitrary addresses
      - This can lead to stolen funds

3.  Controller Risk
    - Ensure controller address is secure to avoid stolen funds

## ERC 621 (Token Standards)

1. ERC 621 totalSupply Control

   - Trusted Actors can increase and decrease the token supply after contract is deployed
     - Uses the increaseSupply and decreaseSupply functions that are specified by the standard

2. Token Supply Risk
   - The total supply of those tokens can be changed after deployment
   - Risk Awareness

## ERC 884 Reissue (Token Standards)

1. ERC 884

   - This Token standard introduces Cancel & Reissue
   - Defines Actors known as Token Implementors who can cancel address within the context of a contract

2. Impementors

   - Move any Tokens owned or held by those addresses to a new address while canceling the older address

3. Risks

   - Token Holding Risk because it can move funds to a new address while canceling your address
   - Risk Awareness

## ERC 884 Whitelisting (Token Standards)

1. ERC 884 Whitelisting Addresses

2. Addresses

   - Whitelisted

3. Token Transfer

   - Only to Whitelisted Addresses

4. Risks
   - Token Transfer Risk because user may not be in the whitelist while the sender may want to transfer at the same time
   - Risk Awareness

## Asset Limits (Guarded Launch)

1. Guarded Launch

   - Guarded lanuch is critical in the web3 world

2. Launch

   - During launch, the amount of assets that are managed by the smart contract app are lower at first
   - Over time the amount of assets is increased

3. Launch Time

   - Higher Risk of exploits or bugs during launch time

4. Risk Mitigation
   - Guarded launch while gradually increasing the asset limits

## Asset Types (Guarded Launch)

1. Guarded Launch

   - Asset Types

2. Launch

   - Launch with fewer asset types
   - Over time increase the asset types in a certatin manner

3. First

   - Allow known assets
     - i.e. Safe, Known and acknowledged by the community

4. Risk Mitigation
   - Gradually Increase the asset types

## User Limits (Guarded Launch)

1. Guarded Launch User Limits

2. Launch

   - Few/Trusted Users allowed to use app
     - Usually allow through a whitelist

3. Launch Time

   - Higher Risk initially which can result in exploits

4. Risks
   - Risk Mitigation is best to gradually increase users

## Usage Limits (Guarded Launch)

1. Guarded Launch

   - Usage Limits

2. Launch

   - Limited usage at initial launch
   - Over time the usage increases
   - Usage Examples
     - Tx Size
     - Tx Volume
     - Daily Limit
     - Rate Limiting

3. Risk Mitigation
   - Gradually increase usage

## Composability Limits (Guarded Launch)

1. Guarded Launch Composability Limits

2. Launch

   - Limited composability limits
   - Over time increase the composability
   - First
   - Only allowed to be composed of or allowed of known protocols
   - Later
     - Others

3. Risk Mitigation
   - Gradually Increases

## Escrow (Guarded Launch)

1. Guarded Launch Escrowed Funds

2. High-Value Tx

   - Escrow

3. Timelock/Gov

   - Revert

4. Risk Mitigation
   - Intially Escrow

## Circuit Breaker (Guarded Launch)

1. Guarded Launch Circuit Breaker
   - Emergency
     - Pause
   - Recover
     - Unpause
   - OpenZeppelin Pausable
     - Library to allow the pausing of a contract
2. First

   - Pause/Unpause with Circuit Breaker Approach

3. Later

   - No Circuit Breaker

4. Risk Mitigation
   - Initially pause/unpause

## Emergency Shutdown (Guarded Launch)

1. Guarded Launch Emergency Shutdown

2. Emergency

   - Shutdown

3. Reset

   - Allows one to reset and restart applications

4. First

   - Capability
   - Later
     - Remove

5. Risk Mitigation
   - Emergency Shutdown

## System Specification (Application Level)

1. Requirements

   - Necessary to define a Specification

2. Why & How

   - Spec <-> Requirements

3. No Spec

   - If there is no specification then there is no baseline

4. Requirements
   - Requirements necessary for the design
   - Design the application to specify the requirements
   - Specify then evaluate

## System Documentation (Application Level)

1. Implementation

   - Documentation

2. What & How

   - Implement <-> Document

3. Covers

   - Assets managed by that system
   - Actors within the context of that system
   - Actions that these actors perform
   - Trust Model
   - Threat Model

4. Design Flow
   - Specify
   - Implement
   - Document
   - Evaluate

## Function Paramaters (Application Level)

1. Function Parameters

   - Ensure that proper input validation has been performed

2. Public/External Functions

   - Should be tested especially which can taint the values
     - Perform Taint Analysis

3. Best Practice
   - Make sure there are valid sanity and threshold Check
   - Ex
     - Check for zero address with address input parameter
   - Check for malicious, accidental, incorrect, invalid values

## Function Arguments (Application Level)

1. Function Arguments

   - Call Sites

2. Arguments Vs Parameters

3. Callers Vs Callees

4. Arguments
   - Arguments at the call site should match validity and order

## Check Function Calls (Application Level)

1. Public

   - External
   - Internal
   - Private

2. Strictest Visibility

3. Public/External

   - Anyone can use which can result in vulnerabilities
   - Use <-> Abuse
     - Byzantine Threat Model

## Function Modifiers (Application Level)

1. Modifiers

   - Used for Access Control & Validation
   - Effects Logic And Control Flow By
     - Missings
     - Incorrect/Order

2. Flow

   - Control Flow
     - Could effect control flow by reverting
   - Data Flow
     - Validate data passed which effects data flow

3. Best Practice
   - Ensure correct modifiers are used on correct functions in correct order

## Function Returns (Application Level)

1. Function Call

   - Return
   - Return Values

2. Return Values

   - Correct & All Paths

3. Call Sites

   - Ensure that functions that return values use values and do not ignore those values

4. Best Practice
   - Check returned values
   - Use all returned values

## Function Timeliness (Application Level)

1. Function Calls

   - Timeliness
     - When can these functions be called

2. Public/External Function Calls

   - Can be called anytime

3. State Transitions

   - Assumptions on When to call functions

4. When
   - Arbitrary and Robust Handling to track which state system is in
     - This allows functions to be called in a timely manner

## Function Repetitiveness (Application Level)

1. Function Calls

   - Repetitiveness refers to the amount of times the function is expected to be called

2. Public/External

   - Called Any Number of Times

3. State Transitions

   - Assumptions on number of calls

4. How Many

   - Arbitrary

5. Best Practice
   - Use Initializer Modifier that is discussed earlier

## Function Order (Application Level)

1. Function Calls

   - Order
     - Which + When

2. Public/External

   - Can be called in any order

3. State Transitions

   - Assumptions on Order need to be payed attention to

4. Order
   - Arbitrary Robust Handling

## Function Inputs (Application Level)

1. Function Calls

   - Inputs, what data function calls work with

2. Public/External

   - Called with any inputs

3. Assumptions on Validity

4. Input
   - Arbitrary input validation

## Conditionals (Application Level)

1. Conditionals

   - Result in the control flow
   - i.e.
     - if
     - else
     - for
     - while
     - do
     - break
     - continue
     - return

2. Predicates & Expressions

   - Variables & Operators

3. E.g.
   - || Instead of &&
   - Check Conditionals

## Access Control Spec (Application Level)

1. Access Control

   - Assets
   - Actors
   - Actions

2. Spec

   - Who can access what
   - Why should they have that access
   - When can they have that access
   - How much of the assets can the actors access

3. Trust Model and Threat Model

   - Model & Assumptions

4. Access Control Spec Flow
   - Spec -> Implement -> Enforce -> Evaluate

## Access Control Implementation (Application Level)

1. Access Control Spec

   - Implemented uniformly on all actors and assets

2. Implement/Enforce Actors

   - Assets
   - No Missing
     - Actors
     - Assets
     - Flows
     - Conditions

3. Access Control Spec Flow
   - Spec -> Implement -> Enforce -> Evaluate

## Access Control Modifiers (Application Level)

1. Access Controls Modifiers

   - Enforce the access control

2. Modifiers

   - Encapsulate repetitive checks
   - Schools of thought
     - Good for Auditability
       - Allows for the auditability to be done once which can be good for the auditor to focus on specific logic within functions
     - Bad for Auditability
       - Believe that switching context does not lead to good auditability
   - Modularity Vs Auditability

3. Present & Valid & Correct

## Modifiers Implementations (Application Level)

1. Modifiers Incorrect Implementation

2. Roles & Privileges

3. Correct Checks & Roles & Composition

4. Ensure Correct Implementation

## Modifiers Usage (Application Level)

1. Modifiers Incorrect Use

2. Modifiers Use Case

   - Which Modifiers are used
   - Why are those modifiers used
   - What and How are those parameters are used in the modifiers
   - Order of modifiers when more then one is present
   - When and where should the modifiers be used based on the state transition

3. Correct Functions & Modifiers & Parameters

4. Ensure Correct Usage

## Access Control Changes (Application Level)

1. Access Control Correct Changes

2. Change

   - Assets
   - Actors
   - Actions

3. Risk
   - Wrong address used when accessing or access during an invalid state transition can lead to loss or locking of funds
   - Impact
     - Loss or Lock Funds
4. Best Practices
   - Validate correctness of access control changes
   - Two-Step process to allow recovery from mistakes
   - Log changes for transperancy and offchain tracking
   - Ensure correct changes

## Comments (Application Level)

1. Code Comments

   - Documentation should be well documented
   - Inline & Natspec Comments
   - Details & Relevance

2. Readability & Maintainability

3. Comments Descriptions
   - Code and comments should directly align
   - Discreprencies between code and comments should be addressed
   - Remove stale or Commented Code

## Testing (Application Level)

1. Software Testing Validation

   - Unit Test
   - Functional Test
   - Integration Test
   - Regression
   - E2E
   - Smoke testing
     - Indicates at a high if the functionality works
   - Stress Testing
     - Validates Extreme Scanarios
   - Performance & Security Testing
     - Validates performance or security
   - Testnet Vs Mainnet
     - Remove testing parameters which can introduce bugs when deploying to mainnet

2. Test Vs Production
   - Sufficient Testing

## Unused (Application Level)

1. Unused Constructs
   - i.e.
     - Imports
     - Contracts
     - Functions
     - Variables
     - Events
     - Returns
2. Benefits of Removing Unused

   - Reduce Gas
   - Improve Auditability
   - Improve Maintainability

3. Missing Logic & Assumptions

   - Remove or Use unused constructs
   - Unused constructs could result in vulnerabilities

4. Best Practice
   - Use or remove the unused constructs

## Redundant (Application Level)

1. Redundant Constructs

   - Redundant code or comments can cause confusion

2. Reduce Gas

   - Improve Auditability
   - Improve Maintainability

3. Missing Logic & Assumptions

   - Remove or Use unused constructs
   - Redundant constructs could result in vulnerabilities

4. Best Practice
   - Use or remove the redundant constructs

## ETH (Application Level)

1. ETH Handling

   - Contracts that accept manage or transfer ether should be used appropriately
     - i.e.
       - Deposit
       - Withdraw
       - Transfer
   - msg.value
     - a global variable within the context of a transaction
       - When used or accounted multiple times has resulted in vulnerabilities
   - payable
     - Should account that either less or more ether in payable functions
   - withdraw
     - Account should be maintained correctly
   - balance
     - Account should be maintained correctly
   - transfer
     - Transfers should be reeentrancy safe so that ETH cannot be locked within a contract
   - Reentrancy
   - Locking
   - Access Control
   - Input Validation
   - Error Handling

2. Contracts
   - Contracts/Functions
   - Ensure Correct ETH Handling

## Tokens (Application Level)

1. Token Handling

   - Deposit
   - Withdraw
   - Transfer

2. Types of Tokens

   - Token Functions
   - Decimals of precission
   - Hooks
   - Return Values
   - Fungibility
   - Deviations from Specifications
   - All of Which could result in
     - Reentrancy
     - Locking
     - Access Control
     - Input Vallidation
     - Error Handling

3. Actors

   - System Actors
   - Trusted Vs Untrusted
     - Use <-> Abuse
   - Actors -> Assets -> Actions
   - Specify & Implement & Evaluate
   - All the trusted actors there roles and capabilities should be clearly specified in Trust Vs Threat
     - This is a critical consideration in web3's Byzantine Threat Model

## Privileged Roles (Application Level)

1. Privileged Roles/Actions

   - Deploy/Modify/Pause/Shutdown/Withdraw/Whitelist

2. EOA Vs MultiSig
   - EOA
     - Single Point of Failure
   - MutliSig
     - Brings in Privilege Seperation which is tolerant to a few of the few holder being compromised

## Privileged Roles (Application Level)

1. Two-Step Change
   - One should use a two step approach
2. One-Step Change

   - Error-prone
     - Zero/Incorrecct Address

3. Steps
   - Step 1
     - Old Approves New
   - Step 2
     - New Claims Ownership
   - Error Recovery in Step 1
     - This allows one to mitigate the risk

## Critical Parameters (Application Level)

1. Delay Changes

   - Time lock

2. Immediate Change

   - Unfair
   - E.g.
     - Lower Rewards
     - Increase Fees
   - Event + Time-delay Change
     - Users
       - Exit/Engage offchain based on emitted parameters

3. Best Practice
   - Less Surprise
   - More Fair

## Explicit Vs Implicit (Application Level)

1. Favor Explicit Over Implicit

2. Solidity

   - Explicit function visibility
   - Explicit variable storage

3. App
   - Explicit Spec + Reqs + Validation + Docs
   - Implicit Reqs
     - Assumptions are that they are dangerous

## Configuration (Application Level)

1. Misconfiguration

   - Security Issues

2. Contracts, Parameters, Addresses, Permissions

   - Configurations should be documented and validated

3. Production Vs Test

   - Testing is used with lower levels of threat to validate compared to production

4. Best Practice
   - Check the configuration settings and make sure that they are correct

## Initialization (Application Level)

1. Lack/Incorrect Initialization

   - Security Issues

2. Parameters, Addresses, Permissions, Roles

3. Default/Incorrect Values

4. Check Initialization

## Cleanup (Application Level)

1. Lack/Incorrect Cleanup

   - Security Issues
   - Using solidity's delete keyword
   - Reinitializing variables to default values in the context of the application logic

2. Contract Site

3. State Site

   - Old Values Incorrect can leadReads/Writes

4. Cleanup
   - Provides Gas Refunds
     - London reduced gas refunds of SSTORE
   - Better Security

## Data Processing (Application Level)

1. Processing Issues

   - Security Issues
   - Application Logic Issues
     - Critical or Tainted Data
   - Missed/Incorrect Processing

2. Spec
   - Implemented and Reviewed
   - Check Data Processing

## Data Validation (Application Level)

1. Validation Issues

   - Security Issues
   - Aspects of variable types, low or high thresholds

2. Untrusted Users & Tainted Data

3. Missed/Incorrect Validation

4. Sanity/Threshold Checks
   - Check Data Validation

## Numerical Issues (Application Level)

1. Numerical Issues

   - Security Issues
   - Incorrect numerical computations can lead to issues almost always
     - Overflow/Underflow
     - Precision
     - Casting
     - Parameters/Returns
     - Decimals
     - Bounds/Gas

2. Best Practice

   - Widely-used Libraries
   - These libraries adopt most of the best practices
   - Test thest libraries with Testing/Fuzzing
   - Check Numerical Issues

## Acccounting Issues (Application Level)

1. Accounting Issues

   - Security Issues
   - Incorrect or Insufficient tracking regarding:
     - State
     - Phases
     - Permissions
     - Roles
     - Deposits
     - Withdrawals of funds
   - E.g.
     - Users
     - Balances
     - Rewards/Penalties
     - Fees

2. App Logic

   - Accounting logic related to State Updates/Transitions should be reviewed to ensure that they are correct and complete

3. Spec
   - Implement
   - Check Accounting Issues

## Access Control (Application Level)

1. Access Control
   - Authorization
   - Incorrect or insufficient access control
   - E.g.
     - Users
     - Roles
     - Permissions
     - Modifiers
     - Visibility
     - Address
     - Accounts
     - Keys
2. Assets

   - Actors
   - Actions
   - Trust Models
   - Threat Models

3. Spec
   - Implement
   - Check access control

## Auditing & Logging (Application Level)

1. Auditing & Logging
   - These are important for Monitoring Security of an app
   - In context of Smart Contracts
     - Events/Emits
     - Public Variables
     - Public/External Getters
     - Error Strings
2. Off-Chain & On-Chain

   - Incorrect or Insufficient offchain monitoring can lead to security issues
   - Monitor
   - Detect
   - Recover

3. Correct & Sufficient Audit Logs
   - Needs to be paid attention to
     - Monitor
     - Detect
     - Recover

## Cryptography (Application Level)

1. Cryptographic Primitives

   - On-chain & Off-chain

2. Keys, Accounts, Hashes, Signatures, Randomness

3. ECDSA & Keccak-256

   - More: BLS, RANDAO, VDF, ZK

4. Fundamental
   - Cryptographry is Critical to Security

## Error Reporting (Application Level)

1. Errors

   - Exploit
   - Security Issues

2. Error Conditions
   - Exceptional Behavior not normally encountererd validated or noticed
3. Spec
   - Normal
   - Deviation
     - Leads to Error

## DoS (Application Level)

1. Denial of Service

   - CIA (Confidentiality, Integrity, Availability)
     - Dos effects Availability

2. Users
   - Preventing other users from successfully accessing system services by either modifying system parameters or shared state
   - Affects shared state
     - Results in DoS
3. Effects
   - Lock Funds
   - Lose Profit
   - Tx Inclusion
   - Griefing
     - Spending ether on gas or any other tokens required for DoS interactions
4. Recognize & Minimize DoS Attributes

## Timing (Application Level)

1. Timing Issues
   - Can have a Security Impact
   - Incorrect assumptions on timing of user actions which cannot be controlled
   - Triggering of system state transitions or dependencied on blockchain state or transactions may all lead to issues depending on the context within the app
2. User/Contract/Blockchain/block.timestamp

   - Common blockchain transaction issues

3. Timing Attributes
   - Should be analyzed to avoid dealing with these issues

## Ordering (Application Level)

1. Ordering Issues

   - Incorrect assumptions of ordering of user actions or system state transitions can lead to security issues
   - User Actions
   - State Transitions
   - Transactions

2. Front Running, Back Running, Sandwiching

   - Front Running
     - Front running when the attackers race to finish before the users transaction or interaction
   - Back Running
     - Back Running when the attackers race to finish right after the users transaction or interaction
   - Sandwiching
     - Sandwiching when the attackers transaction or interaction is sandwiched between the interaction

3. Ordering <-> Timing
   - Ordering Attributes and evaluate if they can be abused

## Undefined Behavior (Application Level)

1. Undefined + Malicious

   - Undefined behavior triggered maliciously or accidentally can lead to security issues

2. Specs Definitions

   - In Spec
     - This is defined behavior
   - Not In Spec
     - This is undefined behavior

3. Undefined Behavior

   - If triggered accidentally that may result in a Revert/Exploit
   - Should be treated as a security concern

4. Best Practice
   - Ensure all acceptable behavior is detailed in spec, implemented accordingly, and documented thoroughly

## Interactions (Application Level)

1. External Interactions

   - External Interactions can have a security impact
   - E.g.
     - External Actors
     - External Assets
     - External Actions
   - These interactions may be outside of the Trust/Threat Models making them external

2. Interactions
   - Interactiong with external systems such as
     - Tokens
     - Contracts
     - Oracles
   - This assumes correctness and availability
   - External can effect internal
   - Interactions can have implications
   - Increasing Composability make this a significant challenge

## Trust (Application Level)

1. Trust Minimization

   - Trusted actors may be compromised
   - Foundational value of decentralization of Web3

2. Insider

   - Insiders and outsiders blur due to trust and decentralization

3. Use

   - May lead to misuse under assumption of byzantine threat models
   - May lead to privilege escalation

4. Best Practice
   - Never Trust
   - Always Verify

## Gas (Application Level)

1. Gas Issues

   - When gas limits are exceeded can lead to sDoS
   - This causes a Security Issue

2. Turing Complete

   - Bound Computation

3. Loops, External Calls

   - OOG
     - Out of Gas can lead to failed transfers
     - Out of Gas can lead to locked funds

4. Gas Assumptions
   - Gas Usage must be verified due Security Implications that can lead to DoS

## Dependency (Application Level)

1. Dependency Issues

   - External Factors
   - Imports
   - Contracts
   - Tokens
   - Oracles
   - Relayers

2. Trust, Correctness, Availability
   - Assumptions if broken can lead to security implications
3. Dependencies
   - Should be well documented and evaluated for issues

## Constant (Application Level)

1. Constancy Issues

   - Constant
     - Wont Change
   - Change for some reason
   - Can Occur With:
     - Hardcoded Parameters
     - Hardcoded Assumptions
   - E.g.
     - Block Time
     - Addresses
     - Permissions
     - Roles

2. Constant
   - Any assumed constants changing can lead to security issues if and when they are altered

## Fresh (Application Level)

1. Freshness Issues

   - Freshness of an object is an aspect if it is the latest one
   - Not Stale

2. Tx Nonce

   - Use of nonce in transactions to prevent replay attacks by repeating older transactions

3. Oracle

   - The asset price updates of oracles
     - If Stale
       - Can lead to accounting issues

4. Lack

   - Lack of Timely Update
   - Lack of Availability

5. Best Practice
   - Ensure values from timely updates or available transactions are fresh to avoid security implications

## Scarcity (Application Level)

1. Scarcity Issues

   - Less assets will be secure?

2. Assumptions

   - Incorrect assumptions about such scarcity
     - Tokens funds available to any system actor will lead to unexpected outcomes if assumptions are broken
   - Funds
   - Tokens
   - Users

3. Flash Loans/Mints

   - Susceptibility to flash loans or flash mints related overflows
     - Example where the vulnerable contract makes a scarcity related assumption and applies that to the size or types of variables used to maintain token balances
     - If broken can lead to overflows
   - Sybil Attacks
     - Where an attacker subverts a system by creating multiple accounts

4. Best Practice
   - Scarcity
     - Ensure abundance by checking scarcity assumptions
   - Security Implications

## Incentives (Application Level)

1. Incentive Issues

   - What?
   - How Much?

2. Use <-> Abuse

3. Incentives

   - Incentives to liquidate positions in DeFi lending apps
   - Lack of Incentives may also cause issues
     - DoS
     - Griefing

4. Incorrect Assumptions
   - Incorrect assumptions about incentives about system or external actors to perform or not perform
     - Leads to security issues
5. Clarity

   - Clarity Issues
     - Assets
     - Actors
     - Actions
   - Spec
   - Implementation
   - Documentation
   - UI/UX

6. Less Clarity

   - Less clarity leads to more assumptions which can lead to security issues

7. Best Practice
   - Increasing clarity by specifying, and implementing security

## Privacy (Application Level)

1. Privacy Issues

   - Could be related to
     - Assets
     - Actors
     - Actions

2. Transactions & Data Blockchain

   - Data and transactions on ethereum are not private

3. Mempool

   - Pending transactions in Mempool can also be tracked

4. Privacy Assumptions
   - Incorrect assumptions about privacy aspects of data can be abused leading to security issues

## Cloning (Application Level)

1. Cloning Issues

   - Copying and or pasting code from libraries, contracts, protocols with minimal or no changes
   - Context
   - Assumptions
   - Bugs
   - Fixes

2. Cloning Risks
   - Security Implications

## Logic (Generalizations & Higher-Level)

1. Business Logic

   - Application Specific
   - Translated from requirements to specifications
   - Assumptions
     - Errors

2. Lack of Rules/Toiks

   - Infer Constraints

3. High-Severity
   - High security implications due to their impact

## Principle 1

1. Least Privilege

   - Saltzer & Schroeder 1978

2. Privilege
   - Least set of privileges required for the job should be used
   - More privilege
     - Abuse
     - Exploit
   - Privileges should be need based

## Principle 2

1. Separation of Privilege

   - Saltzer & Schroeder 1978

2. Privileges

   - Where feasible a protection mechanism that needs multiple usera
   - E.g.
     - Multi-Sigs Vs EOA

3. Separation
   - No Single Point of Failure

## Principle 3

1. Least Common Mechanism

   - Saltzer & Schroeder 1978

2. Minimize Sharing
   - Least number of security modules or code are used
   - Common Points of Failure are minimized

## Principle 4

1. Fail-Safe Defaults

   - Saltzer & Schroeder 1978

2. Permission Vs Exclusion
   - Base access decisions based on permission rather than exclusion
   - E.g.
     - Guarded Launch
     - Defaults
       - Visibility
       - Initializations
       - Permissions
       - Assets
       - Actors
       - Actions
3. Open Vs Closed
   - Weigh Pros & Cons

## Principle 5

1. Complete Mediation

   - Saltzer & Schroeder 1978

2. Access Control

   - All Assets, Actors, Actions
   - Ex
     - Missing Modifiers
     - Permissive Visibility
     - Missing Auth Flows

3. Mediation
   - Complete mediations requires access control enforcement on every actor, asset, action on all parts at all times

## Principle 6

1. Economy of Mechanism
   - Saltzer & Schroeder 1978
2. Design/Code

   - Simple
   - Small
   - Readability
   - Security

3. KISS Principle

4. More Complex
   - Less Secure

## Principle 7

1. Open Design

   - Saltzer & Schroeder 1978

2. Open Design/Source

   - Permissionless participation

3. Contract

   - Open-source and verified

4. Security
   - Design/Code
   - No Security by obscurity
   - Byzantine threat model

## Principle 8

1. Psychological Acceptability

   - Saltzer & Schroeder 1978

2. Human Interface

   - Ease of Use UI/UX

3. Humans

   - Can code them and use them

4. Ease

   - Apply Security

5. Design/Flow
   - More Intuitive
   - Less Risk

## Principle 9

1. Work Factor

   - Saltzer & Schroeder 1978

2. Cost of Circumventing

   - Benefit of Exploiting
   - Contracts
     - Rewards M/Billions
     - Low Risk, High Reward

3. Maximum Incentives
   - Maximum Risks/Mitigations

## Principle 10

1. Compromise Recording

   - Saltzer & Schroeder 1978

2. Bug-Free Code

   - Try to Reduce Attack Surface
   - Anticipate Residual Risk
     - Have incidence response plan
     - Monitor & Detect & Fix

3. On-Chain

   - Add Checks

4. Off-Chain
   - Add Events

# Audit Techniques & Tools 101

## Audit

1. External Security Assessment

   - Typically requested and paid for

2. Security Vulnerabillities

3. Pitfalls & Best Practices

4. Software Quality
   - Documentation
   - Subjective readability
   - Composability
   - Design

## Scope

1. Smart Contracts

   - Ethereum based smart contracts
   - Onchain smart contract code typically

2. Offchain Code

   - Offchain code that interacts with contract is also tested

## Goal of Audits

1. Assess & Alert

   - The goal of audit is to ensure that there reduce vulnerabilities
   - Increase security and design of project to avoid adding bugs in the future

2. Security Posture

3. Attack Surface

   - Reduce the amount of areas in which vulnerabilities can occur

4. Mitigate Risk
   - Reduce exposure to ensure that smart contract functions as it is intended to be designed

## Non-Goal of Audits

1. Security Warranty
   - Not a guarantee of bug free code
   - Bug Free
     - An audit tries to find vulnerabilities which are left in the smart contract
   - Best Effort
     - An audit is an effort made to try to reduce the vulnerabilities in a project
   - Constraints
     - An audit has constraints such as time, expertise, and understanding
     - The expertise of auditors significantly effects the audits effictiveness

## Target

1. Project Teams

2. Paying Clients

   - Targeted to project owners
   - Not Project Users

3. Technical/Business Goals
   - What are their incentives
   - Where should clients look for unbiased security

## Need for Audits

1. In-house Expertise

2. Time/Effort

3. External Review

   - Demand for audits orders of magnitude higher than the supply

4. Domain Experts
   - Projects could benefit from expertise to increase efficiency
   - Improve code quality based on specifications

## Types of Audits

1. New/Repeat Audits
   - New Audits
     - New audits are for projects that have just completed and are needed to increase security
   - Repeat Audits
     - Repeat audits are for projects that have been deployed and want to increase security
     - Could also include new needs for features added to projects extensions
2. Fix

   - Fix audit for reviewing the fixes made for a current or prior audit

3. Retainer

   - Retainer audit where the audit is continuously viewing the changes made to the project

4. Incident
   - Incedent audit which review the exploit that has taken advantage of a vulnerability and diagnose the issue

## Timeline Audits

1. Type/Scope/Nature

   - Depends on complexity of project and type of audit requested

2. Timeline
   - Depends on value at risk and complexity
   - Number of Files
   - External dependencies or oracles
   - Complexity of Code
   - SLOC
   - Complex math libraries
   - Familiarity from auditing team

## Effort of Audits

1. Number of Auditors

   - Supplementary and complemantary

2. Expertise/Experience
   - More than one auditor is usually preferred to cover blind spots

## Cost of Audits

1. Type/Scope/Nature

   - Market
   - Demand
   - Supply
   - Strength of Reputation

## Pre-Reqs of Audit

- Clear Scope
- Repository
  - Commit Hash of project files on Git Repo
- Team
  - Team behind project public or anon
- Specification
  - Specification of design and architecture of project
- Documentation
  - The documentation of a projects implementation and associated business logic
- Threat Model
  - Specific areas of concern from the project team
- Prior Reviews
  - Testing done, tools used, and reports from other audits
- Timeline/Effort
  - Timeline, effort, and cost must be agreed upon
- Engagement Model
  - Modes of communication should be agreed upon to avoid confusion
- Point of Contact
  - Single point of contact to make audit possible and seemless

## Limitations of Audits

1. Residual Risk

   - Limited amount of audit time or effort
   - Limited documentation or specification
   - Limited Security Expertise
   - Limited Coverage
   - Could arise from complexity or limited use of tools or knowledge

2. All Audits

   - Not all audits are equal
   - Greatly Depends on expertise of auditors and processes implemented

3. Snapshot

   - Audits provide only a project security snapshot over a short period of time
   - Sometimes smart contracts need changes which include adding possible vulnerabilities

4. Necessary
   - Audits are considered necessary but not sufficient

## Audit Reports

1. Scope/Goals/Effort/Timeline/Approach/Tools

2. Findings/Classification/Severity/Exploits/Fixes

3. Recommendations/Best-Practices

4. Comprehensive Document
   - Provides details of audit conducted
   - Includes severity of bugs

## Classification of Vulnerabilities

### Based on Classification of Trail of Bits

1. Access Control

   - Related to authorization of users and assessment of rights

2. Auditing/Logging
   - Auditing of actions and logging of problems
3. Authentication
   - Authentication of users in context of the application
4. Configuration
   - Configuration of servers devices or software
     - i.e. smart contracts or off chain components
5. Cryptography
   - Cryptography related to protecting the privacy or integrity of data
6. Data Exposure
   - Data exposure related to unintended exposure of sensitive information
7. Data Validation
   - Data Validation related to improper reliance on the structure or values of data
8. Denial-Of-Service (DoS)
   - Related to causing system failure or inaccessability
9. Error Reporting
   - Related to reporting of error conditions
10. Patching

- Related to keeping softwarre up to date using patches

11. Session Management

- Session management related to identification of authenticated users

12. Timing

- Related to race conditions, locking, or order of operations

12. Undefined Behavior

- Categorized as undefined behavior

## Difficulty of Audity

1. Rough Measure of Diffuculty of how likely the vulnerability is to be discovered or exploited by the attacker

2. OWASP
   - Proposes likelihood level
     - low
     - medium
     - high
     - some firms use their own
3. Trail Of Bits
   - low
     - The vulnerability may be easily exploited because public knowledge exists over vulnerability type
     - Related to common security pitfall, or missing best practice at solidity or EVM level
   - Medium
     - Attackers may need an in depth knowledge of the complex system to exploit the vulnerability
       - May be something application specific related to business logic and not a commonly seen or known vulnerability
   - High
     - Attacker must have priveleged or insider access to the system
     - Need to know extremely complex technical details of that system or must discover some other weakness in order to exploit this issue
     - Could imply that one of the privileged roles may be malicious or compromised
   - Undetermined
     - The difficulty of exploit was not determined during the engagement of the audit
     - Could happen due to
       - Nature of vulnerability
       - Context of Application
       - Operational aspects of audit engagement did not allow this to be determined
   - Relative classification is more important
     - Should be consistently applied across audit

## Impact of Vulnaribility

1. OWASP

   - The magnitude of the technical and business impact on the system if the vulnerability were to be exploited
   - Low
   - Medium
   - High
   - Vulnerabilities have higher impact in Web3

2. Web3

   - High
     - Causing loss of funds or locking of funds that may be triggered by any unauthorized user
   - Medium
     - Vulnerabilities that effect the app significantly but do not immediately lead to loss of funds
   - Low
     - Anything is considered low impact
   - Relative impact matters more
   - Should be applied consistently

## Severity of Bugs

1. OWASP Likelihood X Impact
   - 3x3 matrix
   - low-low: Note
   - low-med: Med
   - low-high: High
   - med-low: Med
   - med-med: Mes
   - med-high: High
   - high-low: Med
   - high-med: High
   - high-high: Critical

## Checklist

1. Checklist for projects to get ready for a checklist

   - Test
   - Review
   - Document

2. Test

   - Enable and address every compiler warning
   - Increase Unit and Feature test coverage

3. Internal Review

   - Perform an internal review to address a common security pitfalls and best practices

4. Documentation

   - What does the project do
     - Who uses it
     - Why and how it delivers the functionality
   - Add comments about intended behavior inline with the code
   - Label and describe your tests and results both positive and negative tests
   - Include past reviews and any bugs found
   - Document steps to create a build environment
   - Document external dependencies
   - Document build process including the debugging and test environment
   - Document the deployment process and its environment

5. Communicate
   - Communicate all of our information in suitable ways to an audit firm
   - So that they have all of the info and do not waste time
     - Discussing
     - Requesting
     - Duplicating
     - Addressing aspects

## Analysis Techniques

1. Manual/Automated Analysis
   - Performed with tools
2. Combination

3. Specification Analysis

   - Performed Manually
   - Describes the What/Why aspects of the project and its components
   - What is the project supposed to do functionally as part of the design and architecture as it stems from the requirements
   - What the assets are
   - Where are the assets held
   - Who are the actors in this context
   - Privileges of the actors
   - Whos allowed to access what and when
   - Trust relationships
   - Threat model
   - Potential attack vectors, scenarios and mitigations
   - Analyzing the spec of a project provides auditors with the above details and lets them evaluate assumptions to identify shortcomings
   - Infer
     - Typically lost time for auditors
     - Leaves them with less time for deeper specification

4. Documentation Analysis

   - Performed Manually

5. Software Testing

   - Automated Technique

6. Static Analysis

   - Automated Technique

7. Fuzzing

   - Automated Technique

8. Formal Verification

   - Automated technieque with some manual assistance

9. Manual Analysis
   - Performed entirely manually

## Specification Analysis

1. Performed Manually

2. Describes the What/Why aspects of the project and its components

3. What is the project supposed to do functionally as part of the design and architecture as it stems from the requirements

4. What the assets are

5. Where are the assets held

6. Who are the actors in this context

7. Privileges of the actors

8. Whos allowed to access what and when

9. Trust relationships

10. Threat model

11. Potential attack vectors, scenarios and mitigations

12. Analyzing the spec of a project provides auditors with the above details and lets them evaluate assumptions to identify shortcomings

13. Infer

- Typically lost time for auditors
- Leaves them with less time for deeper specification

## Documentation

1. What/How something has been designed

2. README/Comments

3. Serves as a substitute for a missing specification

4. Understanding Docs helps auditors save time to understand assumptions made into the codebase

5. Infer
   - Project team is highly encouraged to document thoroughly so that auditors do not need to waste time

## Software Testing

1. Common software engineering primitive

2. Determine if software outputs expected outputs

   - Based on chosen inputs
   - Projects have little testing in auditing stage usually

3. Unit/Functional/Integration/E2E/Smoke

   - Different units should be tested due to holding highly vallued assets

4. Test Cases/Coverage
   - Program testing can be used to show the presence of bugs but never their absence

## Static Analysis

1. Analyzing program properties without running program

2. Solidity/EVM

   - Can be performed on solidity or EVM code directly

3. Control + Data Flow
   - E.g.
     - Slither
       - Trail of Bits
     - Maru
       - Consensys Diligence

## Fuzzing

1. Software testing for Fuzzing

2. Random/Invalid Inputs

   - Random inputs

3. Monitor

   - Crashes
   - Failures
   - Leaks

4. Tools
   - Echidna
     - Trail of Bits
   - Harvey
     - Consensys Diligence

## Symbolic Checking

1. Symbolic Inputs

   - To represent a set if states and transitions
   - Instead of using real inputs and enumerating all individual state and transitions seperately

2. Models & Properties

   - The related concept of model checking is a technique to check whether Finite State Models meets a given specification
   - To solve a problem algorithmically must mathematically formulate logic

3. Language & Logic

4. Tools
   - Manticore
     - Trail of Bits
   - Mythril
     - Consensys Diligence

## Formal Verification

1. Proving Correctness of algorithms

2. Formal specification & Methods

   - Use formal methods of math

3. Specific/Deep Properties

   - Effective at detecting complex bugs
   - Generally hard to detect manually
   - Needs spec of program being verified

4. Tools
   - Certora Prover
   - VerX
     - Chain Security
   - KEVM
     - Models EVM semantics

## Manual Analysis

1. Complementary to Automated Analysis

   - Automated analysis using tools is cheap
   - Uses open-source tools

2. Business Logic & Application Constraints

   - Expertise is a rare and expensive skillset

3. Slow & Expensive

   - Not Deterministic and scalable
   - Only way to determine as of now

4. Critical Human Aspect

## False Positives

1. Incorrectly Flagged Vulnerabilities

2. Incorrect Assumptions or Analysis Simplifications
   - Findings which flag the presence of vulnerabilities that are not vulnerabilities
   - Require further verification
3. Increases Effort & Decreases Confidence

   - Could lead to reduced trust in the findings of the auditor

4. True Vs False Positives
   - Findings left as FP may be left due to decreased confidence

## False Negatives

1. Missed Flagging Vulnerabilities

   - Missed findings that should have been reported

2. Incorrect Assumptions or Analysis Inaccuracies

   - Do not correctly consider the minimum factors for presence of vulnerabilities
   - Vulnerabilities can be exploited due to them being missed
   - Increases Risk and Decreases Confidence

3. True Vs False Negatives
   - TN are missed findings or findings that are dismissed because they are not vulnerabilities

## Security Tools

1. Assist Developers & Auditors

2. Potential Vulnerabilities

3. Common Pitfalls

   - Best practices
   - Highlight dangerous programming styles

4. Complement Manual Analysis

### Security Tools Categories

1. Testing

2. Test Coverage

3. Linkers

4. Static Analysis

5. Symbolic Checkers

6. Fuzzing

7. Formal Verification

8. Visualization

9. Disassemblers

10. Monitoring

## Slither Overview

1. Static Analysis Tool

   - Trail of Bits

2. Solidity Analyzer Framework

   - Made with Python3
   - Easy-to-Use
   - Free

3. Solidity/EVM Pitfalls

4. 75+ Detectors
   - Custom Analysis
   - Printers

## Slither Features

1. Vulnerability Detectors

   - Contract Info Printers

2. Low False Positives

3. Runtime < 1 Sec/Contract

4. Continuous Integration

   - Designed to integrate into CI/CD frameworks
   - Implements built-in printers
   - Supports a detector API written in Python

5. SLithIr
   - Intermediate representation
   - Enables simple high-precision analysis

## Slither Detectors

1. 75+ Detectors

   - Each of which detects a particular type of vulnerability

2. Supported Test Frameworks

   - Truffle
   - Embark
   - Dapp
   - Etherlime
   - Hardhat

3. Run/Exclude/ Specific Detectors
   - e.g.
     - reentrancy-eth
     - unprotected-upgrade
   - Basically a filter, similar to grep

## Slither Printers

1. Print Different Types of Contract Info

   - Helps in contract comprhension
   - Provides visibility

2. Control Flow Graph

3. Call Graph

4. Summaries

5. Inheritance

6. Functions, Modifiers, Variables, Dependencies

7. SlithIR, EVM

## Slither Upgradeability

1. Slither check upgradeability
   - Has a specific tool called slither check upgradeability
   - Reviews contracts that use the Delegatecall Proxy pattern to detect potential security issues with upgradeability
     - Delegatecall Proxy/Implementation/V2
   - Variables
     - Missing
     - Extra
     - Order
     - Initialized
   - Init
     - Missing
     - Present and can be called multiple times because of missing initializer modifier
     - Multiple
   - Functions
     - Collisions
     - Shadowing

## Slither Code Similarity

1. Detect Similar Solidity Functions

2. ML

   - Trained Models to detect similar functions
   - Etherscan Verified Contracts used to train
     - 60k Contracts
     - 850m Functions

3. Copy/Fork Vulnerabilities
   - Useful to detect vulnerabilities from code clones, forks, and copies

## Slither Flat

1. Contract Flattening Tool

2. Strategies

   - Most Derived
     - Exporting all most derived contracts
   - One File
     - Helps us export all contracts in one stand alone file
   - Local Import
     - Exports every contract in one seperate file

3. Cicular Dependencies

4. Platforms
   - Truffle
   - Hardhat
   - Etherlime

## Slither-Format

1. Automatic Patch Generation

2. Git Compatible

3. Detectors

   - Unused state
   - Solc Version
   - Pragma
   - External Functions
   - Constable states
   - Constant Function
   - Naming Convention

4. Review & Apply

   - Checks conformance for various ERC standards such as:
     - ERC20
     - ERC721
     - ERC777
     - ERC165
     - ERC223
     - ERC1820

5. Functions

   - Present
   - Return correct type
   - Etc.

6. Events
   - Present
   - Emit correct parameters
   - Indexed
   - Etc.

## Slither-Prop

1. Property Generation Tool

   - Generate Code properties or invariants that can then be used for testing
   - Testing can be done with unit tests or echidna

2. ERC20 Scenarios
   - Check for correct transfer
   - Possible functionality
   - No one can incorrectly mint or burn tokens

## Slither New Detectors

1. Extensible Architecture New Detectors

   - Allows one to integrate new detectors into the tool
   - Skeleton for Common Detector Implementation
     - Argument
     - Help
     - Impact
     - Confidence
     - Wiki

2. \_detect()

   - Placeholder for the Detector logic

3. Extensible Logic
   - Project Specific
     - Create detectors specific to an application
   - Community Contributions
     - Allow the community to contribute new detectors to the slither codebase

## Manticore

1. Symbolic Execution Tool

   - Developed by Trail of Bits

2. Capabilities
   - Symbolic Inputs State Exploration
     - Explore all possible states and reach
   - Input Generation
     - It can produce inputs that result in any desirable program state
   - Error Discovery
     - It can detect crashes and other failures in smart contracts
   - Instrumentation
   - Programmatic Interface

## Echidna

1. Fuzzing Tool

   - Developed by Trail of Bits
   - Developed in Haskell

2. Grammar-based Fuzzing Campaigns
   - Based on a contracts ABI the Echidna tools attempts to falsiy predicates

## Echidna Features

1. Code Tailored Inputs

2. Corpus Collection

3. Coverage/Mutation

4. Guided Exploration

5. Deeper Bugs

6. Slither-Prop Powered

7. Source Code Integration

8. Multiple UI

9. Testcase Minimization

10. Workflow Integration

## Echidna Usage

1. Executing Test Runner Contract + Invariants

   - Takes a contract and a list of invariants as inputs
   - Invariant + Random Calls
     - Provides Counterexamples
     - Finds a way to falsify the invariant
       - Refers to as Counterexamples

2. Invariant Writing

   - Invariants are expressed as solidity functions with names that begin with echidna\_
   - Have no arguments and return a boolean

3. Collecting/Visualizing Coverage
   - After finishing a fuzzing campaign Echidna can save that coverage maximizing composed in special directory
     - JSON files that can be replayed by Echidna later
     - A plain text file that contains a copy of source code annotated with comments

## Eth Security Toolbox

1. Tools Package

   - A docker container package provided by Trail of Bits
   - Preinstalled and preconfigured

2. Tools Included
   - Slither
   - Echidna
   - Manticore
   - Rattle
   - Ethno

## Ethersplay

1. Binary Ninja Plugin

   - Developed by Trail of Bits
   - Extends a dissasembler to work with EVM Bytecode

2. Input

   - EVM Bytecode

3. Displays
   - Display Control Flow Graphs
   - Displays Manticore Coverage

## Pyevmasm

1. Security Tool

   - Developed by Trail of Bits
   - Provides EVM Assembler and Disassembler

2. Command-line Utility
   - For dissassembly and Assembly
3. Python API
   - For extensibility

## Rattle

1. Security Tool

   - Developed by Trail of Bits

2. EVM Binary Static Analysis Framework

   - Designed to work with deployed smart contracts
   - EVM Byte strings as inputs
   - Flow-Sensitive Analysis

3. Stack
   - SSA Register provides more Readable Code

## EVM CFG

1. Security Tool

   - Trail of Bits

2. EVM Bytecode
   - Extract CFG (Control Flow Graph)
   - Recovers
     - CFG
     - Functions Names
     - Attributes
     - Into a DOT File
3. Used By
   - Ethersplay
   - Manticore
   - Other Tools

## Crytic Compile

1. Security Tool

   - Developed by Trail of Bits

2. Smart Contract Compilation Library

   - Supports
     - Solc
     - Truffle
     - Embark
     - Etherscan
     - Brownie
     - Etc

3. Used By
   - Slither
   - Echidna
   - Manticore
   - Etc

## Solc-Select

1. Security Helper Tools

   - Developed by Trail of Bits

2. Script

   - Used to switch quickly between solc versions

3. Solc-select Manages

   - Install/Switch + Wrapper

4. Official solc Binaries
   - Dowloaded from official registry

## Etheno

1. Testing Tool

   - Developed by Trail of Bits

2. JSON RPC multiplexer

   - Diff Tests
   - Multiple Clients

3. Analysis Took Wrapper

   - Manticore
   - Echidna

4. Test Frameworks
   - Ganache
   - Truffle

## MythX

1. Security Service

   - Developed by Consensys Diligence

2. Paid API-based Service
   - Uses several tools in the backend
     - Maru
       - Static Analyzer
     - Mythril
       - Symblic Analyzer
     - Harvey
       - Greybox Fuzzer
   - Implements 46+ Detectors

## MythX Process

1. API-Based Service

   - Does not run locally on the users machines on cloud

2. Submit Code
   - First step is to submit code to the MythX service
     - The request are encrypted with TLS
     - Expected to submit source code and compiled bytecode for best results
   - Second step is to activate the full suite of analysis techniques behind MythX
     - The longer MythX runs the more security vulnerabilities it can detect
   - Third step is to receive a detailed report behind MythX
     - Provides a user friendly dashboard

## MythX Tools

1. When Submitted
   - When code is submitted to MythX API it gets analyzed by multiple microservices in parallel
   - Three tools cooperate
2. Static Analyzer - Maru
   - Passes the solidity AST for the project
3. Symbolic Analyzer - Mythril
   - Detects all the possible vulnerable states in the project
4. Greybox Fuzzer - Harvey
   - Detects vulnerable execution paths in the smart contract
   - Guided by coverage information
5. Combination
   - Comprehensive analysis using the 3 services

## MythX Coverage

1. SWC Registry

   - Smart Contract Weakness registry

2. Smart Contract Weakness Classification

3. 46+ Detectors

4. Comprehensive Coverage

## MythX SaaS

1. SaaS
   - Security-as-a-service
2. Cloud Vs Local

   - Better Performance compared to running security tools locally because of cloud resources

3. Three Tools

   - Better coverage from 3 tools

4. Continuous Upgrades
   - Different Exploit Vectors lead to new vulnerabilities

## MythX Privacy

1. Contract Code

   - SaaS APIs provide a privacy guarantee to the smart contract code submitted

2. TLS Encryption
   - The MythX stores some of the contract data in its database
     - including source code and byte code
   - That data never leaves the secure server
     - Not shared with outside parties
   - Results
     - Authorized access only for team submitted

## MythX Performance

1. Performance

   - Performance is a security issue because it may require many resources and time to be able to deeply assess the smart contract
   - MythX can be configured for three types of scans

2. Configurable Scans
   - Quick Scans
     - Run for 5 minutes
   - Standard Scans
     - Run for 30 minutes
   - Deep Scans
     - Run for 90 minutes

## MythX Versions

1. MythX Versions

   - Comes in different versions to be accessed in multiple ways

2. CLI

   - CLI provides unified tool access to MythX

3. Library

   - JS/TS Integrations

4. PythX
   - Python library to access MythX
5. VSCode
   - Extension to scan/view directly from the code editor

## MythX Pricing

1. On-Demand

   - USD 9.99 for 3 scans

2. Developer

   - USD 49/month for 500 scans

3. Professional

   - USD 249/month for 10k scans

4. Enterprise
   - Custom pricing discussed with Consensys Diligence

## Scribble

1. Verification Tool

   - Consensys Diligence

2. Scribble Language
   - Scribble is a verification language and a run-time verification tool that translates high-level specs into solidity
   - Annotations
     - Assertions
   - Principles
     1. The specification should be easy to understand by developers and smart contract security auditors
     2. Specification should be simple to reason about
     3. Specification should be efficiently checked using off the shelf analysis tools
     4. A small number of code specification constructs should be sufficient to reason about more advanced constructs
3. Instrumental + Equivalent Contracts
   - Runs Tools
     - Harvey
     - Mythril
     - MythX

## Fuzzing-as-a-Service

1. Fuzzing Service

   - A service provided by Consensys Diligence

2. Specifications

   - Embedded inline specifications written using the scribble language

3. Submit

   - Fuzzing of smart contract code needs to be submitted

4. Campaigns

   - Run using the harvey fuzzer
   - Using techniques to optimize fuzzing campaigns

5. Receive/Fix Violations
   - Violations are received for the project to fix them

## Karl

1. Security Tool
   - Security Tool from Consensys Diligence
   - Can be used to monitor Ethereum Blockchain
   - New Deployed Contracts
2. Run Mythril

   - Karl checks for security vulnerabilities using the Mythril detection engine
   - Can be an interesting montoring tool for detecting vulnerable deployed smart contracts

3. Report Vulnerabilities in Real-Time

## Theo

1. Security Tool

   - Developed by Consensys Diligence

2. Exploitation Tool
   - An exploitation tool with metasploit-like like interface
   - Reconnaisance
     - Exploit
     - Frontrunning/Backrunning transactions

## Visual Auditor

1. Visual Studio Extension

   - Developed by Consensys Diligence

2. Security-Aware Syntax

   - Semantics Highlighting

3. Code Review/Reporting/Augmentation

4. Solidity & Vyper

## Surya

1. Visualization Tool

   - Developed by Consensys Diligence

2. Generates

   - Call Graphs
   - Inheritance Graphs

3. Integrated w/ Visual Studio Code Auditor

4. Commands
   - graph
   - ftrace
   - flatten
   - describe
   - etc.

## SWC Registry

1. Smart Contract Weakness Classification

2. Aligned to Web2 CWE Structure & Terminology

3. Goal
   - Common Language
   - Classification
   - Compare & Improve tools

## Securify

1. Security Scanner developed by ChainSecurity

2. Static Analysis

3. Written in Datalog

4. 38+ Detectors

## VerX

1. Verification Tool

   - Temporal Safety Properties

2. Reduction

   - Temporal Safety Verfication to Reachability checking
   - Efficient Symbolic Checking Engine

3. Delayed Abstraction

## SmartCheck

1. Security Tool

   - Developed by SmartDec

2. Extensible Static Analyzer

   - Static Analysis tool for discovering vulnerabilities and other code issues in Ethereum Smart Contracts written in Solidity

3. XML-based IR (Intermediate Representation)
   - An interesting implementation aspect is that it translates solidity source code into an XML-based solidity representation
   - XPath Pattern Checking

## K-Framework

1. Verification Framework
   - From the Runtime Verification Team
   - Includes
     - KEVM
       - Model of EVM in K-Framework
     - First Executable EVM Specification
   - Framework for Building Tools

## Certora Prover

1. Formal Verification
   - A formal verication tool provided by Certora
   - Checks that a smart contract satisfies a set of rules
     - Rules
       - Written in Specify Language
       - Symbolic Checking
2. Prover

   - All Paths/Inputs
   - Or produces a test input known as a Counterexample

3. Abstract Interpretation & Constraint Solving

## HEVM

1. EVM Implementation

   - Developed by DappHub
   - Implementation of EVM made for testing & debugging

2. Test

   - Unit
   - Property

3. Interactive Debugging

## CTFs

1. Capture the Flags

   - Fun/Edu Challenges

2. Hack Dummy Contracts w/ Vulnerabilities

3. Capture the Ether

   - A set of challenges tests knowledge of ethereum contracts

4. Ethernaut

   - Developed by OpenZeppelin
   - Try to hack levels

5. Damn Vulnerable DeFi

   - A set of DeFi related challenges
   - Created by Tincho

6. Paradigm CTF
   - Set of 17 challenges

## Security Tools

1. Assist Humans

2. Automate Tasks

3. Fast

4. Cheap

5. Scalable

6. Deterministic

7. Common Pitfalls & Best Practices

## Audit Process

1. Read Spec/Docs

   - Understand requirements, design and architecture behind aspects of the project

2. Fast Tools

   - Run fast automated tools such as Linters or static analyzer to investigate common security pitfalls

3. Manual Analysis

   - Manually analyze the code to understand the business logic aspects and detect vulnerabilities in it

4. Slow/Deep Tools

   - Running slower but more deeper tools
     - Symbolic checker
     - Fuzzer
     - Static Analyzer

5. Discuss Findings

   - Made more auditors discussing other findings
   - Identify False Positives

6. Convey Status

   - The Auditors may also convey status to the project team

7. Iterate

   - All these aspects may be iterated as many times as possible
   - Leave some time for writing the report

8. Deliver Report

   - The audit team delivers the report to the project team
   - Discuss the findings, serverities and possible fixers

9. Evaluate Fixes
   - The audit team evaluates fixes from the project team for any of the findings reported
   - They verify that any of those fixes remove the vulnerabilities

## Read Spec/Docs (Audit Process)

1. Requirements/Design/Arhcitecture

2. Specification Vs Documentation

   - Specification starts with the projects business goals and requirements
     - Specification describes the why
   - Documentation is a description of what has been happening based on what has been happening
     - Documentation describes the how
   - Encouraging Projects to make provide a detail specification and documentation

3. Absence

   - Absence of documentation or specification can lead auditors to infer those aspects
   - Can lead to wasted time/effort

4. Assets & Actors & Actions
   - Identifying the key assets and actors and logic
   - All of this takes up a lot of time

## Fast Tools (Audit Process)

1. Linters, Static Analyzers

   - Run in Seconds

2. Common Pitfalls

   - Best Practices

3. Control/Data Flow

   - False Positives
   - False Negatives

4. Evaluating the Findings is a good starting point
   - False Positives are possible
   - These tools can miss certain findings
   - E.g.
     - Slither
     - Maru

## Manual Analysis (Audit Process)

1. Manual Code Review is required to understand business logic

   - Missed Flagging Vulnerabilities

2. Business Logic & Application Constraints

3. Implementation Vs Spec/Documentation

4. Infer Constraints

## Slow/Deep Tools (Audit Process)

1. Fuzzing/Symbolic Checking/Verification

2. Custom Properties

   - Run in Minutes

3. More Prep/Expertise

   - Deeper Analyses

4. E.g.
   - Manticore
   - MythX
   - Echidna
   - Harvey
   - Scribble

## Discuss w/ Auditors

1. "Given enough eyeballs all bugs are shallow"

2. Independent Vs Group

3. Bias & Effectiveness

4. Overhead Vs Overlap

## Discuss w/ Project Team

1. Open Communication Channel

2. Clarify Assumptions

3. Discuss Findings/Impact/Fixes

   - Have weekly sync up calls in multi-week audit

4. Update Status
   - Do not let them steal attention

## Write Report

1. The Audit report is a finding compilation of the entire system

2. Presents all aspects of the audit

   - Audit Scope
   - Coverage
   - Timeline
   - Team
   - Effort
   - Summaries
   - Tools Used
   - Techniques
   - Findings
   - Exploit Scenarios
   - Suggested Fixes
   - Short-term and Long-Term Recommendations
   - Any appendices with any tools and rationale
   - Scope

3. Summary & Details

   - An executive summary typically gives an overview of the audit report with highlights, lowlights, illustrating the number and type severity of vulnerabilities found
   - Overall asessment of risk
   - It may also include descriptions of
     - Smart Contracts
     - Actors
     - Assets
     - Roles
     - Permissions
     - Access Control
     - Interactions
     - Threat Model
     - Existing Risk Mitigation Measures

4. Findings

   - Severity
   - Scenarios
   - Suggestions

5. Quality

   - Coding
   - Conventions
   - Coverage

6. Articulate & Actionable
   - Actionable for the project team to address all raised concerns

## Deliver Report (Audit Process)

1. Publish & Present

   - The delivery of the audit report is another important aspect of the audit process

2. Final Milestone

   - This will be the project team will have access to the assessment details
   - The delivery typically happens with a shared document

3. Agree on Findings/Severity

4. Review & Resond

5. Private/Public
   - Depends on the teachers of the audit process

## Evaluate Fixes (Audit Process)

1. Findings

   - Accept
   - Acknowledge
   - Deny

2. Fixes

   - Recommend
   - Review

3. Evaluation

   - Time & Timeline

4. Ensure Security

## Manual Review

1. The Most Critical Component of Smart Contract Audits

2. Different Approaches

3. Access Control

4. Asset Flow

5. Control Flow

6. Data Flow

7. Different Focus

8. Inferring Constraints

9. Dependencies

10. Assumptions

11. Checklists

## Access Control (Manual Review)

1. Fundamental Security Review

2. Who has access to What?

   - Actors -> Assets

3. Roles

   - Admins
   - Users
     - Critical roles have access to critical functionality
   - Visibility
     - Public
     - Private
     - Internal
     - External
   - ## Modifiers

4. Checking For
   - Correct
   - Complete
   - Consistent

## Asset Flow (Manual Review)

1. Assets

   - ETH
   - ERC20
   - ERC721 tokens

2. Who/When/Which/Why/Where
   - Questions to Ask
   - Who
     - Assets should be withdrawed/deposited only by authorized specialized addresses as specified by application logic
   - When
     - Assets should be withdrawed/deposited only by specialized time windows or under authorized specialized conditions as per application logic
   - Which
     - Assets only those authorized specialized types should be withdrawn/deposited
   - Why
     - Assets should be withdrawn/deposited only for authorized/specified reasons as per application logic
   - Where
     - Assets should be withdrawn/deposited only to authorize specified addresses as per application logic
   - What Type
     - Assets only off authorized types should be withdrawn/deposited as per the logic
   - How Much
     - Assets only in authorized/specified amounts should be allowed to be withdrawn/deposited again as per the application logic

## Control Flow (Manual Review)

1. Transfer of Control

   - Execution Order

2. Intra/Inter Procedural

   - Typically Indicated by a Callgraph which shows which functions callers call which other functions or callees
   - Dictated by Conditionals & Loops and return statements

3. Control Flow Graph
   - Help track flow of execution and data in smart contracts
   - Fundamental program analysis approach to evaluate security aspects

## Data Flow (Manual Review)

1. Transfer of Data
   - Analyzes the transfer of data across and within smart contracts
   - If the procedural data flow is evaluated by analyzing the data
     - Variables and Constants used as argument values for
     - Function Arguments and callsites & Return Values
   - Intra procedural data flow is evaluated by analyzing the assignment and use of variables or constants stored in
     - Storage/Memory/Stack/Calldata along control flow paths within functions
2. Both intra and infra Procedurual Data Flow analyses
   - Help track the flow of global or local storage memory changes in smart contracts

## Inferring Constraints (Manual Review)

1. Program Constraints

   - Rules/Properties that should be followed by the program

2. Solidity/EVM Vs Application Constraints

   - Solidity level and EVM level Security Constraints
     - Well known because they are part of the language
   - Application Level Constraints
     - Rules that are implicit to the business logic implemented
     - May not be explicitly described in the specification

3. Lack of Spec/Documentation
   - Makes auditors infer
4. Maximal Occurence
   - Inference
   - Evaluate whet is being done on most program parts related to a particular logic and treat that as a constraint

## Dependencies (Manual Review)

1. External Code/Data
   - Dependencies exist when the correct compilation of functioning of program code relies on code or data from other smart contracts that were not necessarily developed by project team
   - Explicit program dependencies are captured in the import statements and the inheritance hierarchy
2. Libraries/Protocols/Oracles

3. Composability

   - Composability in Web3 is expected and encouraged
   - Smart Contracts interfacing with other protocols
     - Results in Emerging or implicit dependencies on the state logic of external smart contracts
     - Interest of Concern for DeFi Protocols that rely on other related protocols for stablecoins, yield generation, borrowing, lending, oracles

4. Assumptions on Functionality/Correctine
   - Assumptions on the functionality and correctness of dependencies need to be review for potential security impact

## Assumptions (Manual Review)

1. Incorrect Assumptions

   - Who can access what and when

2. Who/What/When/Why etc.

3. Verify Assumptions

   - Identifying Assumptions of Audit Code and Verifying they are indeed correct can be source of bugs

4. E.g.
   - Admins
     - Only Admins can call these functions
     - Initialization Functions will only be called once by the contract deployer
   - Order
     - Functions will only be called within a certain order as expected by spec
   - Input Validation
     - Parameter will only have Non-Zero Values
     - Parameter will only have Values within a certain threshold
     - Ex
       - Address will never be certain value ex zero
   - Reach
     - Certain addresses or values will never reacch locations where they can be misused
     - Known as Taint Analysis
   - Return Values
     - Function calls will always be successful so checking for return values is not required

## Checklists (Manual Review)

1. Itemized Lists

   - Checklists are lists of Itemized points that can be quickly and methodically followed
   - Referenced later by the list number
     - To make sure all list numbers have been processed
   - Distinction
     - Errors of Ignorance
       - Mistakes We Make because we do not know enough
     - Errors of Ineptitude
       - Mistakes We Make because we do not make proper use of what we know

2. Retention & Recall

   - Smart Contract Security Experts need checklists also
   - Smart Contract Security Checklists will help in navigating the vast number of key aspects to be remembered and applied

3. No Missed Checks
   - Help in attacking specific chances

## Exploit Scenarios (Manual Review)

1. Proof-of-Concept

   - Incidents where vulnerabilities are triggered by malicious acctors

2. Written Descriptions/Code

   - Presenting PoCs of such code make audit findings more realistic or relatable by eliciting explicit exploit paths
     - Justifying the severity of findings

3. Reasonable & Responsible

4. Realistic & Relatable

## Likelihood & Impact (Manual Review)

1. Likelihood

   - Probability & Difficulty

2. Impact

   - Magnitude of Implications

3. Severity

   - Likelihood + Impact

4. Access & Assumptions, Funds Vs Functioning

## Audits Summary (Manual Review)

1. Bounded Effort

   - Time
   - Resource
   - Expertise

2. Automated & Manual

3. Findings

   - Difficulty
   - Impact
   - Severity

4. Shows Presence
   - Not Absence

# Audit Findings 101

## Consensys Diligence Audit (1)

1. Audit on Aave V2 Finding 5.4

2. Error Handling

3. Medium Severity

4. Unhandled transfer/transferFrom

   - Unhandled return values on functions using ERC20 Tokens
   - ERC20 tokens should always return values to anticipate inconsistencies

5. Use SafeERC20 Wrappers
   - Safer to Use OpenZeppelin's SafeERC20 wrapper functions

## Consensys Diligence Audit (2)

1. Consensys Audit

   - DeFi Saver Finding 5.1

2. Reentrancy

   - Critical Severity
   - Users DSProxy allowed the user to write a DSProxy
   - Performing a reentrancy attack by detecting any task of choice leading to users funds being

3. Malicious External Calls
   - Integrating any task of choice
4. Add Reentrancy Guard
   - Recommendation was to add Reentrancy Guard from OpenZeppeling

## Consensys Diligence Audit (3)

1. Consensys Audit

   - DeFi Saver Finding 5.2

2. Input Validation

   - Major Severity

3. Tokens w/ >18 Decimals
   - Not common but could cause invalid errors
4. Use SafeMath
   - Fixed by using the safemath sub function that reverts tokens with less than 18 decimals

## Consensys Diligence Audit (4)

1. Consensys Audit

   - DeFi Saver Finding 5.3

2. Error Handling

   - Major Severity

3. Function Return Values
   - Unchecked Error Codes
   - Error codes were never checked in certain control flows
4. Solution
   - Check Error Code
   - Revert if Necessary
   - Check function and return values in security pitfalls

## Consensys Diligence Audit (5)

1. Consensys Audit

   - DeFi Saver Finding 5.4

2. Ordering

   - Medium Severity

3. Incorrect Parameter Ordering

   - The use of the reversed order of parameters were not in the same order as safeTransferFrom

4. Solution
   - Fix Ordering
   - Fixed by swapping the order of parameters

## Consensys Diligence Audit (6)

1. Consensys Audit

   - DAOfi Finding 4.1

2. Input Validation

   - Critical Severity
   - Token approvals can be stolen in the ad liquidity function of a protocol
     - Created the desire pair contract if it did not already exist then transfer tokens into the pair
     - There was no validation to to transfer tokens from
     - Could be used to add liquidity to a pair contract for which the attacker was the pair owner
     - Allowing stolen funds using the pair function

3. No Address Validation

   - Token Transfer

4. Solution
   - Transfer tokens from msg.sender instead of LPsender

## Consensys Diligence Audit (7)

1. Consensys Audit

   - DAOfi Finding 4.4

2. Error Handling

   - Major Severity
   - Swap exact tokens for ETH checked the wrong return value
   - Instead of checking that the amount of tokens received from a swap was greater than the minimum amount expected from the swap
   - It calculates the difference between the initial receivers balance and the balance without

3. Solution
   - Recommendation was to check the intended values
   - We have discussed this aspect of correctly checking intended values

## Consensys Diligence Audit (8)

1. Consensys Audit

   - DAOfi Finding 4.5

2. Denial-of-Service

   - Medium Severity
   - The DAOfi pair deposit function accepted deposits of zero amounts blocking the pool there after
   - This was because the function allowed only a single deposit to be made
     - And no liquidity could ever be added to the pool after the deposit variable was executed
   - The Deposit function did not check for a non-zero function amount
     - This allowed a malicious user that did not hold any tokens to lock the pool by calling deposit without first transferring any funds to the pool

3. Solution
   - Require a minimum deposit with non-zero check
   - Always check inut validation

## Consensys Diligence Audit (9)

1. Consensys Audit

   - Fei Finding 3.1

2. Application Logic

   - Critical Severity
   - The genesis group commit function overwrote previously commited values
   - Overwrote Value instead-of adding value
   - This allowed anyone to change instead of adding to the value
     - This let anyone change a value to zero instead of adding any value

3. Solution
   - Add to Existing Value instead of overwriting

## Consensys Diligence Audit (10)

1. Consensys Diligence Audit

   - Fei Finding 3.2

2. Timing

   - Critical Severity
   - Purchasing and committing after launch was impossible
   - Which meant that even after the genesis group launched had successfully been executed
     - it was still possible to invoke genesis group purchase and commit functions

3. Solution
   - State-tracking
   - Function Validation
     - Ensuring that the functions could not be called after launch

## Consensys Diligence Audit (11)

1. Consensys Audit

   - Fei Protocol Finding 3.3

2. Data Validation
   - Major Severity
   - Fei performed some mint burn operations via UniSwap incentive and incentivize functions
   - Which calculated buy/sell incentives using Overflow prone math and then minted burn from the target based on the results
   - Any Overflows would have had unintended functions on such minting or burning
   - Overflow-prone Casting
     - Unsafe casting by user supplied uint256 argument to int256 which is a down cast and could have overflown
3. Solution
   - Use SafeCast to avoid overflow

## Consensys Diligence Audit (12)

1. Consensys Audit

   - Fei Protocol Finding 3.4

2. Timing

   - Medium Severity
   - Bonding Curve allowed users to acquire Fei before Genesis Launch
     - where its allocate function could be called before Genesis Launch if the contract had a non-zero ETH balance
   - By sending even 1 wei anyone could bypass checks and mint Fei

3. Solution
   - Prevent Allocate from being allowed to be called before Genesis Launch
   - Related to ordering issues
   - Misuse of a contracts ETH balance

## Consensys Diligence Audit (13)

1. Consensys Audit

   - Fei Protocol Finding 3.5

2. Error Handling

   - Medium Severity
   - The issue was that this time ended function returned true even if the timer had not been initialized
   - Timed start-time was set only when init-time was called
   - This time-ended function was called using ended time of zero
     - Even if timer had not been initialized

3. Solution
   - Return True even if the timer had not been started

## Consensys Diligence Audit (14)

1. Consensys Audit

   - Fei Protocol Finding 3.6

2. Data Validation

   - Medium Severity
   - Using many Math Operations without using SafeMath

3. Solution
   - Use SafeMath or Compiler >= 0.8

## Consensys Diligence Audit (15)

1. Consensys Audit

   - Fei Protocol Finding 3.7

2. Error Handling

   - Medium Severity
   - There was no checking for the return value of transfer call
   - Unchecked Return Value ERC20 transfer

3. Solution
   - Add require or Use SafeERC20 Wrapper

## Consensys Diligence Audit (16)

1. Fei Protocol Finding 3.8

2. Timing
   - Medium Severity
   - Genesis Group Emergency Exit function remained functional after launch
     - Emergency Exit was intended as an escape mechanism for users in the event that the genesis failed or froze
     - Emergency Exit and launch were intended to be mutually exclusive but were not because either of them remained callable
3. Solution
   - Ensure that launch cannot be called if emergency exit has been called and vice versa
   - Related to Ordering Issues
   - Related to Timing Issues

## Consensys Diligence Audit (17)

1. Consensys Audit

   - bitbank Finding 5.1

2. Error Handling

   - Major Severity
   - ERC20 tokens that did not return a value would fail to transfer
   - Incorrect Return Value Check on ERC0 Transfer

3. Solution
   - Use SafeERC20 Wrapper

## Consensys Diligence Audit (18)

1. Consensys Audit

   - MetaSwap Finding 4.1

2. Reentrancy

   - Major Severity
   - This Reentrancy vulnerability was in MetaSwaps Swap Function were an attacker was able to reenter swap they could execute their own trade

3. Solution
   - Use Reentrancy Guard
   - Where non reentrant modifiers are used on swap

## Consensys Diligence Audit (19)

1. Consensys Audit

   - MetaSwap Finding 4.2

2. Access Control

   - Medium Severity
   - Malicious Adaptor could access User Tokens
   - Initial Purpose of MetaSwap
     - Could save users gas costs when dealing with a number of different aggregators
   - Risk in design was that an existing or newly added maliciuous or buggy adaptor would have access to all users tokens

3. Solution
   - Redesign token approval architecture by making MetaSwap contract the only contract that receives token approval
   - Related to Token Handling
   - Related to Trust Issues

## Consensys Diligence Audit (20)

1. Consensys Audit

   - MetaSwap Finding 4.3

2. Timing
   - Medium Severity
   - A malicious or compromised owner could front-run traders by updating adaptors to steal from users
   - Users had to fully trust every adaptor
3. Solution
   - Disallow Modifications of exising adaptors but instead add new adaptors and disable the old ones
   - Related to Transaction Order Dependence Aspect
   - Related to Time-Delay Change of Critical Contract Aspects
   - Related to Trust Aspects

## Consensys Diligence Audit (21)

1. Consensys Audit

   - mstable-1.1 Finding 6.2

2. Timing
   - Major Severity
   - Abuse of Sliding Window
     - Users could collect interest by only staking m tokens from
     - When users deposit m assets in return for lending ETH and swap fees users received credit tokens at an exchange rate
       - Exchange rate was bigger than possible
       - However it an enforced a minimum timeframe of 30 minutes in which the interest would not be okay
   - User who deposited shortly before end of timeframe would receive credits at stayed interest rate and withdraw at favorable rate after 30 minute window
     - This would make users to benefit from interest payouts by only staking m assets momentarily
3. Solution
   - Remove 30 minute window such that also every deposit also updated the exchange rate between credits and tokens
   - Related to System Design to Anticipate/Prevent Abuse

## Consensys Diligence Audit (22)

1. Consensys Audit

   - Bancor V2 Finding 5.1

2. Timing

   - Critical Severity
   - Oracle updates that could be manipulated to arbitrage rate changes by sandwiching the oracle update between two transactions
   - Sandwich attack
     - First transaction send the higher gas price than the oracle update transaction so as to front run it would convert a very small amount
     - Second transaction sent at a slightly lower gas price than the transaction that updated the oracle so as to backrun it and effectively sandwich it
       - Would perform a large conversion at the wold stayed wake
       - Add a small amount of liquidity to trigger rebalancing
       - The attacker could convert back at the new rate
       - The attacker could update liquidity for step two and use a flash loan

3. Solution
   - Not allow users to train at a stayed oracle rate and trigger an oracle update in the same transaction
   - Related to transaction order dependence
   - Related to Ordering aspect

## Consensys Diligence Audit (23)

1. Consensys Audit

   - Shell Protocol Finding 6.2

2. Input Validation

   - Major Severity
   - Where certain functions lack input validation
   - Parameter checks
     - uint should be larger than zero when zero is considered invalid
     - unit should be within constraints or thresholds
     - int should be positive in some cases
     - length of arrays should match if more than one related are set as arguments
     - addresses should not be zero addresses

3. Solution
   - Add input validation
   - Length of arrays should match if more than one related arrays are set as addresses
   - Add checks and ensure that all inputs are validated

## Consensys Diligence Audit (24)

1. Consensys Audit

   - Shell Protocol Finding 6.3

2. Access Control

   - Major Severity
   - Related to access control
   - Several functions that gave extreme power to the protocol administrator
   - The most dangerous was the one granting capability were administrator could
     - malicously or accidently deploy code
       - This could break the whole pool or lock up the users and LPs tokens
     - The function SafeApprove allowed the administrator to move any of the Users tokens in the contract to any address
       - which could be used as a backdoor to completely drain the contract

3. Solution
   - The recommendation was to remove the SafeApprove function and improve users trust by making the code static and unchangeable after deployment
   - Make Code Static
   - Increase Trust
   - Related to least privilege principle
   - Related to separation of privilege principle
   - Related to Access Control and Trust Issues

## Consensys Diligence Audit (25)

1. Consensys Audit

   - Lien Protocol Finding 3.1

2. Denial-of-Service
   - Critical Severity
   - Reverting Fallback function would lockup all payouts
   - Reverting ETH Transfer Batch Failure
   - Entire payout would fail and be unrecoverable
3. Solution
   - Recommendation was to implement a pull withdrawal pattern or ignore a failed transfer leading to responsibility up to the recipients
   - Related to DoS
   - Related to ETh Handling Functions
   - Related to Concerns with Calls within loops leading to DoS
   - Reviewed OZ pull payment library which specifically deals with this issue

## Consensys Diligence Audit (26)

1. Consensys Audit

   - The Lao Finding 5.1

2. Denial-of-Service
   - Critical Severity
   - Related to DoS
   - Issue was related to safe ragequit and ragequit functions used for withdrawing funds from the Lao
   - The difference between them was that SafeRageQuit
