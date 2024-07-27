# Solana Keypair, Airdrop, Transfer, and Program Interaction Project


## Transaction Link

Success! Check out your TX here:[here](https://explorer.solana.com/tx/4ksfxdTkmZjKQs8XyRKhGQ4E5RLyrzLosBKvLbNR8hw1sFSuphstVzQ2sDU5bCZVX23HiXzZAjGzDHRHkHSRHDrW?cluster=devnet)

## Project Overview

This project involves creating and interacting with Solana wallets using TypeScript. It includes scripts to:

- Generate a new Solana wallet keypair.
- Airdrop SOL tokens to the generated wallet.
- Transfer SOL tokens between wallets.
- Enroll a GitHub account into a program on the Solana devnet.

## Project Structure

- `keygen.ts`: Generates a new Solana wallet keypair and prints the public and private keys.
- `airdrop.ts`: Requests an airdrop of 2 SOL tokens to the generated wallet.
- `transfer.ts`: Transfers 0.1 SOL from the generated wallet to another wallet.
- `enroll.ts`: Interacts with a program on the Solana devnet to enroll a GitHub account.

## Getting Started

### Prerequisites

Ensure you have Node.js and yarn installed on your system. You can install `touch-cli` globally to create files easily:

```bash
npm install touch-cli -g
```

Setup

    Create a new project directory and navigate into it:

   ``` bash

mkdir airdrop && cd airdrop
```
Initialize a new TypeScript project:

```bash

yarn init -y
```
Install the required dependencies:

```bash

yarn add @types/node typescript @solana/web3.js bs58
yarn add -D ts-node
```
Create the necessary TypeScript files:

```bash

touch keygen.ts
touch airdrop.ts
touch transfer.ts
touch enroll.ts
```
Initialize the TypeScript configuration:

```bash

yarn tsc --init --rootDir ./ --outDir ./dist --esModuleInterop --lib ES2019 --module commonjs --resolveJsonModule true --noImplicitAny true
```
Update package.json to include scripts for running the TypeScript files:

json

    {
      "name": "airdrop",
      "version": "1.0.0",
      "main": "index.js",
      "license": "MIT",
      "scripts": {
        "keygen": "ts-node ./keygen.ts",
        "airdrop": "ts-node ./airdrop.ts",
        "transfer": "ts-node ./transfer.ts",
        "enroll": "ts-node ./enroll.ts"
      },
      "dependencies": {
        "@solana/web3.js": "^1.75.0",
        "@types/node": "^18.15.11",
        "typescript": "^5.0.4"
      },
      "devDependencies": {
        "ts-node": "^10.9.1"
      }
    }

Running the Scripts
Generating a Keypair

Run the following command to generate a new Solana wallet keypair. The public and private keys will be printed to the console:

```bash

yarn keygen
```
Save the private key in a dev-wallet.json file for future use.
Claiming an Airdrop

Run the following command to request an airdrop of 2 SOL tokens to your generated wallet:

```bash

yarn airdrop
```
Transferring SOL

Run the following command to transfer 0.1 SOL from your generated wallet to another wallet:

```bash

yarn transfer
```
Enrolling in the Program

Run the following command to enroll your GitHub account into the program on the Solana devnet:

```bash

yarn enroll
```
Keeping Your Wallet Secure

Ensure you keep the secret key of the Devnet wallet safe to access this wallet in the future.




