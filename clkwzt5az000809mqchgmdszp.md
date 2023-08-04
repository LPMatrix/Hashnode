---
title: "Simplifying Operations with Tatum's Key Management System (KMS)"
datePublished: Fri Aug 04 2023 19:42:36 GMT+0000 (Coordinated Universal Time)
cuid: clkwzt5az000809mqchgmdszp
slug: simplifying-operations-with-tatums-key-management-system-kms
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1690937931822/f3e73235-3ba7-4826-8f9d-e6d59f259fad.png
tags: security, cryptocurrency, kms, tatum, tatumkms

---

## Introduction

In the world of cryptocurrency exchanges and applications, custodial wallets offer a convenient way for users to interact with their digital assets without the complexities of managing private keys. Tatum's Key Management System (KMS) is a robust solution that simplifies custodial wallet management, ensuring security and scalability for seamless operations.

## Secure Wallet Generation and Storage

Tatum KMS provides a reliable mechanism for generating and securely storing wallet data, each associated with a unique signatureId. This signatureId represents a single wallet, whether mnemonic or private key-based. The system supports up to 25,000 signatureIds per API key, allowing for efficient handling of various wallets.

The private keys and mnemonics are stored in an encrypted file called wallet.dat in the local file system. Tatum KMS employs the AES-GCM-256 cipher to ensure robust encryption and protection of wallet data.

## Flexibility through CLI and Daemon Modes

Tatum KMS offers two modes of operation, providing added flexibility for different use cases:

1. CLI Mode: Ideal for wallet and private key generation, the CLI mode simplifies initial setups and one-time operations.
    
2. Daemon Mode: Geared towards ongoing operations, the daemon mode regularly fetches pending transactions from the Tatum API. It then signs these transactions locally and broadcasts them to the blockchain, streamlining the workflow for efficient custodial management.
    

## Authentication Made Easy with Signature IDs

Tatum KMS simplifies authentication through three types of signature IDs:

1. Private Key-based Signature IDs: Instead of using the privateKey directly, users can utilize the corresponding signatureId tied to the mnemonic for signing operations.
    
2. Mnemonic-based Signature IDs (for Virtual Accounts): Users can use the signatureId associated with the mnemonic to sign operations, reducing complexity and enhancing security.
    
3. Mnemonic & Index-based Signature IDs: When both a mnemonic and an index are required to sign an operation, Tatum KMS handles this by utilizing the signatureId matching the mnemonic and its corresponding index.
    

## Note on SignatureId Capacity

Tatum KMS allows efficient management of up to 25,000 mnemonics or private keys per API key. Each mnemonic can contain up to 2^32 addresses, ensuring the capacity to securely handle 25,000 x 2^32 distinctive addresses or customers, enhancing scalability for custodial operations.

## Enhanced Security Measures

The `wallet.dat` file containing wallet keys and mnemonics is password protected, ensuring an added layer of security for sensitive data.

## Installation

### Install KMS via Docker

`docker pull tatumio/tatum-kms`

In the home directory, create a `.env` file with the following parameters and replace the placeholders with your values:

```plaintext
# required
TATUM_API_KEY=XXXXX-YOUR-API-KEY
# one of the following setups is required: password, VGS, Azure, or AWS
# password setup
TATUM_KMS_PASSWORD=XXXXPASSWORD
# VGS setup
TATUM_KMS_VGS_USERNAME=XXXXUSERNAME
TATUM_KMS_VGS_PASSWORD=XXXXPASSWORDVGS
TATUM_KMS_VGS_ALIAS=XXXVSGALIAS
# Azure setup
TATUM_KMS_AZURE_SECRETVERSION=XXVERSION
TATUM_KMS_AZURE_SECRETNAME=XXSECRETNAME
TATUM_KMS_AZURE_VAULTURL=XXXXVAULTURL
# AWS setup
TATUM_KMS_AWS_REGION=us-east-1
TATUM_KMS_AWS_SECRET_NAME=YOUR_KMS_SECRET_NAME
TATUM_KMS_AWS_ACCESS_KEY_ID=AKIAYWGKDBVRGMCASWIE
TATUM_KMS_AWS_SECRET_ACCESS_KEY=ZxDq62BZGyGe2CzwnVjL/IH8NnJG5Fu0isN7wev9
TATUM_KMS_AWS_SECRET_KEY=pwd
```

## Seamless Workflow with Tatum KMS Commands

Tatum KMS provides a set of easy-to-use commands for managing wallets and signing transactions:

1. Generate a Wallet: Use the command `docker run -it --env-file .env -v $HOME:/root/.tatumrc tatumio/tatum-kms generatemanagedwallet ETH --testnet` to create a new managed wallet for Ethereum on the testnet.
    
2. Create a Private Key: Generate a private key with the command `docker run -it --env-file .env -v $HOME:/root/.tatumrc tatumio/tatum-kms getprivatekey [signatureId] --testnet`.
    
3. Generate an Address: Obtain a new address associated with a signatureId of the private key using the command `docker run -it --env-file .env -v $HOME:/root/.tatumrc tatumio/tatum-kms getaddress [signatureId] --testnet`.
    
4. Store Private Key: Store the private key to your wallet with the command `docker run -it --env-file .env -v $HOME:/root/.tatumrc tatumio/tatum-kms storemanagedprivatekey ETH --testnet`.
    
5. Export the Wallet: Safely export the wallet data using the command `docker run -it --env-file .env -v $HOME:/root/.tatumrc tatumio/tatum-kms export --testnet`
    

## Signing Transactions with the Daemon Mode

By running Tatum KMS in the daemon mode, you can effortlessly fetch and sign transactions periodically. To monitor specific chains, use the `--chain` flag, and adjust the signing frequency with the `--period` flag.

`docker run -it --env-file .env -v $HOME:/root/.tatumrc tatumio/tatum-kms daemon --testnet`

## Conclusion

Tatum's Key Management System (KMS) empowers crypto exchanges and applications with a secure and scalable solution for managing custodial wallets and private keys. Whether in CLI mode for initial setups or the daemon mode for ongoing operations, Tatum KMS streamlines the custodial workflow, providing a seamless and efficient experience for users.