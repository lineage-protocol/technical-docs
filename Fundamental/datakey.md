## Datakey Generation

Lineage Protocol is using a deterministic hash function to generate a unique identifier for each NFT. This identifier, called the "datakey," is based on the NFT address, token ID, chain ID, and nonce.

Using a deterministic hash function has several benefits, including making it possible to verify the integrity and authenticity of the data, and ensuring that the same data always generates the same hash. This can be useful for a variety of applications, including digital signatures, data authentication, and proof-of-existence.

In the context of Lineage Protocol, the datakey provides a unique identifier for each NFT, which can be used to manage and update the metadata associated with that NFT. It also helps to ensure that the metadata is authentic and has not been tampered with, as any changes to the metadata would require a new datakey to be generated.

Overall, using a deterministic hash function to generate the datakey is a key component of Lineage Protocol, providing a secure and reliable way to manage and verify NFT metadata.

### Format

Datakey used in the Lineage node is a deterministic cryptographic hash based on the SHA256 algorithm. It is created by hashing together four pieces of information: the NFT address, the NFT token ID, the chain ID, and a nonce

Formula

```
datakey = sha256(NFT address + NFT token id + chain id + nonce)
```

Result

```
f5e5b12134d36778ac2e0328a4677f14ef59e965631d03dedce355182a012525
```

### Write

To add or update metadata for an NFT, they use their private key to sign a message containing the new metadata, along with the datakey of the NFT. This message is then broadcast to the Lineage network, where it is processed by the appropriate services (such as the DHT service and IPFS DAG service) to update the metadata associated with that datakey.

### Read

To retrieve the metadata for an NFT, they can use the datakey to look up the metadata in the Lineage network.
