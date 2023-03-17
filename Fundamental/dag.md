## IPFS DAG

The Lineage Node makes use of IPFS DAG to store the metadata content of each NFT. The IPFS DAG (Directed Acyclic Graph) is a Merkle DAG (Merkle Directed Acyclic Graph) that provides a content-addressable file system. Each file, directory or symlink in the IPFS DAG is identified by a unique CID (Content Identifier) that is calculated from the file's content using a cryptographic hash function.

The use of IPFS DAG in the Lineage Node provides a secure and resilient way to store the metadata content of NFTs in a decentralized network of nodes. The use of IPFS DAG allows for easy retrieval of the metadata content, and provides a high level of security by storing the data across multiple nodes in the network.

### How it works

When a user creates or updates the metadata of an NFT, the data is first converted to a JSON object, which is then converted to a DAG using IPFS. The resulting CID is stored in the DHT service along with the datakey and public key, allowing the metadata to be easily retrieved using the datakey.

The Lineage Node uses IPFS DAG as a decentralized storage solution, allowing the metadata content to be stored in a distributed network of nodes instead of a centralized server. This provides a higher level of security and resilience as the data is replicated across multiple nodes, making it difficult for attackers to compromise the system.

### Retrieving Metadata

To retrieve the metadata of an NFT from the IPFS DAG, the Lineage Node makes use of the IPFS DAG get command. This command takes a CID as input and retrieves the corresponding DAG from the IPFS network.

Once the DAG has been retrieved, it can be parsed to extract the metadata fields, which can then be formatted according to the Opensea standard, ERC721 or any custom standard as needed.

### Benefit

Using IPFS DAG has several benefits for Lineage node. First, it allows for the metadata to be stored in a decentralized manner, without relying on a central server or database. This reduces the risk of fraud and centralization in the NFT ecosystem, as there is no single point of failure or control.

Second, IPFS DAG provides content-addressable storage, which means that each piece of data is identified by a unique content identifier (CID) that is derived from the data itself. This makes it easy to verify the integrity and authenticity of the metadata, as any tampering or modification to the data will result in a different CID.

Finally, IPFS DAG provides efficient and fast retrieval of metadata, as it uses a distributed hash table (DHT) to locate the data based on its CID. This means that Lineage node can quickly access the metadata from any IPFS node in the network, without having to rely on a centralized server.

### Reference

- https://docs.ipfs.tech/concepts/merkle-dag/
