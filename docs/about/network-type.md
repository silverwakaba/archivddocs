---
sidebar_position: 3
---

# Network Type

Due to the nature of ArchivD which offers two different types of storage network, which in the form of centralized and decentralized storage network, we need to explain the differences between the two in integration as our product.

## Centralized Network

As the name suggests, in this type of storage network all activities are centralized and focused on one location only.

We chose to use a centralized storage network because it is easier to maintain, scalable and has affordable operational costs. We focus this storage network for free and premium users.

But activities and needs such as storage, bandwidth and location will be fully served by only just one server location. Currently our centralized storage network is located somewhere in Europe.

### CDN

This of course provides uneven performance. Users in Europe may be able to experience faster download speeds, but not for users outside Europe.

Therefore, for centralized storage networks, the download process will be powered with the help of CDN technology.

Currently we use two well-known CDN providers, namely BunnyCDN and Fastly. Please adjust to the Point of Presences (POPs) closest to your location from these two CDN providers to enjoy maximum download speeds.

You can access information about their POPs location via the following page:

- [BunnyCDN Network](https://bunny.net/network/)
- [Fastly Network](https://www.fastly.com/network-map/)

Please remember that the CDN providers above can change at any time based on our internal decisions.

## Decentralized Network

As the name suggests, in this type of storage network all activities are not centralized and not focused on one location only, but rather on many locations and devices that are connected to each other in one massive peer-to-peer communication.

We chose to use a decentralized storage network because it offers better security, performance and speed compared to centralized storage networks. However, because the costs are often unpredictable and greater than centralized storage networks, we focus this storage network only for premium users.

In a decentralized storage network, a file is not stored on one physical device or one location, but is split into several parts on many physical devices that are connected to each other whose locations are spread throughout the world.

Each file gets split into 80 pieces, and retrieving a file only requires 29 of those pieces. Each of piece is stored on a different node; all with different operators, power supplies, networks, location and geographies. Currently, over 16.000 nodes are being hosted in 80+ countries are interconnected.

These parts of the file will later be stored encrypted using AES-256-GCM encryption.

These parts of the file can no longer be accessed by anyone until someone request to downloads it. This happens because the file decryption and reconstruction process only occurs during the download process.

Splitting files into pieces means your data is never stored in one place, ensuring ultimate security and availability. If there is a massive power outage, or something causes several nodes to go offline, it is completely fine. The network then will automatically repairs each piece and recreates it on a healthy node ensuring data is never lost. And because each piece is indistinguishable from any other files pieces without the encryption key, this enables unparalleled security and privacy.

Because the performance, speed and technology are similar (or sometime better) to CDN, these decentralized storage networks will not be served along with any CDN.