# Merkle-Tree-Blockchain

This project implements a blockchain-based system for storing and accessing data securely. Here's an overview of the classes and their functionalities:

## `Merkle_Main`

This class handles the major implementation of the code by calling methods from various classes based on user's choice via a switch case menu.

- **Case 1:** Inserts data into a singly linked list (SLL) with only the table name as the data in the SLL node.
- **Case 2:** Displays all the data stored in the SLL.
- **Case 3:** Generates a secret key for accessing classified data stored in the blockchain. Data is displayed only if the key matches for the respective company.
- **Case 4:** Allows tracing back to the origin of a product by scanning the blockchain-generated QR code.
- **Case 5:** Displays the Merkle root node hash, which is public.

## `MerkleTree`

This class describes the functionality and implementation of a Merkle Tree, a tamper-proof data structure. It creates a Merkle Tree only if the number of child nodes entered by the user is a power of two. Hash values of children and parent nodes are stored in ArrayLists. Parent hash values are calculated based on the position of child nodes in the ArrayLists. The Merkle Tree ensures data integrity by comparing child and parent node hash values with pre-calculated hash values. Access to data is granted if the root node matches the public root node hash.

## `Block`

Represents a block in the blockchain, containing fields such as timestamp, previous hash value, and table name. This block is used to insert data of type Node in the SLL.

## `Connection`

Establishes a connection between the SQL databases and the Java code for data retrieval and storage.

## `GenerateQR`

Generates a blockchain-generated QR code used for tracing back to the origin of a product. Encodes a bit matrix and formats it to a barcode image.

## `HashAlgorithm`

Utilizes the SHA-256 hashing algorithm to generate hash values stored in the Merkle Tree for respective table names in the SLL.

## `Node` and `Node1`

Represent nodes used in different contexts. `Node` is used in the Merkle Tree, while `Node1` represents blocks inserted into the SLL.

## `SLL1`

Creates a singly linked list with table names as data stored in the nodes. Blocks are added to the back of the SLL, establishing connections to SQL databases.

## How to Use

1. Run `Merkle_Main.java`.
2. Use the switch case menu to perform various operations such as data insertion, display, access control, tracing, and viewing Merkle root hash.

## Dependencies

- Java Development Kit (JDK)
- SQL Database

Feel free to explore and modify the code to fit your specific use case. For any questions or assistance, please refer to the code comments or contact the author. Enjoy using the blockchain implementation for secure data management!
