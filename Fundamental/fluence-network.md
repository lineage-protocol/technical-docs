## Fluence Network

Provide an overview of the custom Fluence network node used in Lineage, detailing its various capabilities and how it is used to host multiple Wasm services. Discuss how these services are designed to handle different aspects of NFT metadata management.

Fluence is a decentralized computing platform that provides a distributed compute network where users can host and run services, and where services can communicate with each other in a peer-to-peer network. Fluence is used as a backbone of Lineage node to facilitate the development of decentralized applications (dApps) by providing a secure, scalable and fault-tolerant environment for hosting Lineage services. This allows Lineage to provide a decentralized metadata management system for NFTs.

The main feature of Fluence that enables Lineage to achieve its goals is the Fluence Marine VM. It is a WebAssembly-based virtual machine that allows multiple services to run simultaneously on a single node, enabling easy management of multiple services. Each service can communicate with other services using the p2p library, which provides a secure and reliable communication layer between the services.

### Marine VM

Marine is a modern general purpose Wasm runtime based on the component model capable of running multi-module Wasm applications, aka services, with interface-types and a shared-nothing linking scheme. This execution model is well suited for a variety of scenarios and especially applicable to implementations following the entity component system (ECS) pattern or plugin-based architectures.
Reference: https://github.com/fluencelabs/marine

### Libp2p

libp2p is a modular networking stack and library in Go that simplifies the development of peer-to-peer (P2P) applications. It provides a set of protocols and components that can be combined and customized to create decentralized applications.

libp2p offers a wide range of features including peer discovery, peer-to-peer communication, routing, and content distribution. It is designed to be protocol agnostic, which means that it can support various P2P protocols such as BitTorrent, IPFS, and Ethereum.

One of the key features of libp2p is its ability to handle network address translation (NAT) traversal, which is necessary for peers behind different NAT devices to communicate with each other. It also supports encrypted communication through the use of secure transport protocols such as TLS and Noise.

In the context of Lineage, libp2p is used as the underlying network layer for communication between nodes. It enables Lineage nodes to discover and communicate with each other in a decentralized manner, without the need for a central server or intermediary.

Reference: https://libp2p.io/

To connect to Fluence, Lineage node is using the Fluence Client API, which is a Javascript API for interacting with the Fluence network. This API allows Lineage to interact with Fluence services, which are hosted on Fluence nodes. Lineage services are written in Aqua, which is a high-level language that allows developers to write secure and distributed services on the Fluence network.

### Benefit

The use of Fluence network allows Lineage to achieve several key advantages over traditional centralized systems. By using Fluence, Lineage can provide:

- Highly scalable
- Fault-tolerant infrastructure for hosting services (smart contract),
- Secure
- Reliable communication layer between the services.

In summary, Fluence provides Lineage with the necessary infrastructure to build a decentralized metadata management system for NFTs. It allows Lineage to host and manage its services in a highly scalable, fault-tolerant and secure environment, while also enabling easy communication between services. Fluence is an integral part of the Lineage ecosystem, providing a solid foundation for the development of decentralized applications.

### Key services

### Reference

- https://fluence.dev/docs/build/introduction
