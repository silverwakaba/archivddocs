---
sidebar_position: 1
---

# Security

All files stored by ArchivD are protected by a very high level of data security and can only be accessed if the file owner allows them.

All files are then stored in centralized and decentralized storage network, depending on the users preferences and services used.

## Global Security

The security features below apply to all stored files regardless of differences in users preferences and services used.

### Encryted Connection

All files downloaded will be served via an SSL encrypted connection.

### IAM Policy

All files downloaded by request will be served based on Identity and Access Management (IAM) Policy which is used for managing request tokens; Means each download has a unique token that can be used to identify the request such as file location, expiration time and requesting user.

If the token does not match the recorded request, the download request will be automatically rejected and will not be able to be downloaded.

### Unique Identifier

All files stored by ArchivD stored with a unique name and link using the UUID format which can reduce bruteforce attack attempts in file scanning without permission.

This file name will later be adjusted to the original file name when someone downloads.

## Decentralized Security

Plus all of general security, the security features below only apply to all stored files on decentralized storage network.

### Encrypted

We automatically encrypts all files before being uploaded, so your data is only in your hands and those you share it with.

Every file is encrypted using AES-256-GCM symmetric encryption. This is standard on every file before being uploaded to the network which is why no unauthorized user can access your data, so that your data can only be viewed by those who have been granted access.

### Piece by Pieces

After being encrypted, each object is split into pieces that are indistinguishable from any other file objects pieces. This also gives your data constant availability.

Each file gets split into 80 pieces and retrieving a file only requires 29 of those pieces. Each of piece is stored on a different node, all with different operators, power supplies, networks, and geographies. Splitting files into pieces means your data is never in one place, ensuring ultimate security and availability.

If there is a massive power outage or something causes several nodes to go offline, that is not a big deal. Our decentralized storage network will automatically repairs each piece and recreates it on a healthy node ensuring data is never lost. And because each piece is indistinguishable from any other files pieces without the encryption key, this enables unparalleled security and privacy.