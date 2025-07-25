---
layout: page
title: Merkle trees in a blockchain system
description: Efficient verification of blockchain transactions and data integrity using Merkle tree hashing.
img: assets/img/merkle_tree.png
importance: 2
category: data science
related_publications: true
---

Blockchain technology, foundational to cryptocurrencies like Bitcoin, relies on a robust and efficient data structure to manage transactions. A core component of a blockchain is the block, which fundamentally consists of two main parts: the **block header** and the **transaction list**. While the block header contains crucial metadata such as the previous block hash, timestamp, difficulty target, and nonce for proof of work, it also importantly includes the **Merkle root**, which serves to summarize all transactions within that block. The transaction list, conversely, enumerates all transactions contained within the block, commencing with the coinbase transaction that rewards the miner. A significant challenge in managing these blocks arises when considering the scale of transactions.

## The Fundamental Problem: Verification Efficiency and Storage Optimization

Imagine a blockchain block containing thousands of transactions. Without an efficient organizational method, verifying a single transaction would necessitate downloading and checking every single transaction within that block. This approach is highly inefficient in terms of computational resources and time. This inefficiency underscores a fundamental problem in blockchain systems: **how to verify transaction integrity and presence quickly and efficiently without demanding excessive computational load or storage from every participant**.

## The Merkle Tree Solution: A Hierarchical Approach

This fundamental problem is precisely what the Merkle tree is designed to solve. A Merkle tree effectively organizes transactions into a hierarchical tree structure. This structure allows for the verification of individual transactions or subsets of transactions by requiring only a small portion of the data, specifically the Merkle root and a few relevant hash values. Consequently, the verification process becomes significantly faster and more storage-efficient.

## How Merkle Trees Work

The construction of a Merkle tree is a systematic process. Each individual transaction (e.g., T1 to T10) is first hashed to generate a corresponding leaf node. These leaf nodes are then paired and hashed together to form parent nodes. This hierarchical process of pairing and hashing continues upwards through the tree until a single, final hash, known as the **Merkle root**, is produced at the top. This Merkle root comprehensively summarizes all transactions within the block and is subsequently stored within the block header. A critical feature of this structure is its integrity: if even a single transaction (e.g., T1) is altered, it will affect the entire tree structure and update the Merkle root hash, thereby ensuring data integrity across the block.

<img src="/assets/img/merkle_tree_diagram.png" alt="Merkle Tree Structure" style="width:75%; display:block; margin:auto;">

## The Role of SHA-256 Hashing

The integrity and security of the Merkle tree are underpinned by the hashing function employed. In blockchain systems like Bitcoin, the **SHA-256** (Secure Hash Algorithm 256-bit) cryptographic hash function is widely used. SHA-256 possesses three key properties that make it ideal for this application:

- **Fixed Output Size:** Regardless of the input data's size, SHA-256 consistently produces a hash output of a fixed 256 bits.
- **Collision Resistance:** It is computationally infeasible to discover two different inputs that produce the exact same hash output.
- **One-Way Function:** It is almost impossible to reverse engineer the original input data from its hash value.

These properties ensure that any minor change in transaction data results in a completely different Merkle root, immediately signaling a discrepancy.

<img src="/assets/img/merkle_tree_SHA.png" alt="SHA" style="width:75%; display:block; margin:auto;">

## Space Optimization and Simplified Payment Verification (SPV)

One of the significant benefits of the Merkle tree is its contribution to storage optimization. Once transactions are deeply embedded within a block and effectively "buried," the detailed transaction data itself can be removed from a node's storage. Crucially, the Merkle root, which encapsulates the integrity of these transactions, remains stored in the block header. To verify the existence and integrity of a single transaction at a later point, only a few specific branches of the Merkle tree are needed, rather than the entire transaction list. This approach saves considerable storage space while still definitively proving the transaction's inclusion and validity. This mechanism is particularly vital for enabling **Simplified Payment Verification (SPV)**, which allows lightweight nodes to efficiently verify transactions without the necessity of downloading and storing the entire blockchain.

## Transaction Verification Process

The process of verifying a transaction using a Merkle tree is elegant. To verify a specific transaction, it is first hashed. Then, using its corresponding proof (a set of sibling hashes from the Merkle path), the Merkle root is reconstructed. If this newly reconstructed Merkle root precisely matches the Merkle root already stored in the block header, the transaction is confirmed as valid and included in that block.

## Conclusion

In summary, Merkle trees are an indispensable data structure in blockchain systems, widely implemented in networks like Bitcoin. They fundamentally address the challenges of transaction integrity, verification efficiency, and scalability by allowing for rapid and secure validation of transactions with minimal data transfer and storage requirements. Beyond blockchain, their utility extends to distributed storage systems for efficient data verification. The ingenious design of the Merkle tree has proven to be a cornerstone for robust and decentralized digital ledgers.

---

## Further Reading / Video

[Video: Merkle Trees Explained](https://youtu.be/YV5rhi04aqs?si=bHbwhYCFXuzU1HHF)

[Demo Notebook: Merkle Tree Python Demo](https://github.com/joe8606/merkle_tree/blob/main/merkle_tree_demo.ipynb)


