# Assignment Table Checklist

| Mark | Output                                                                                                                                                                                                                                    | Location                                                                            |
| ---- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| 5%   | Setting up Ethereum account (public address and private key to be provided for Node.JS application)                                                                                                                                       | documents/ethereum_testnet_address_of_owner.txt documents/encrypted_private_key.txt |
| 5%   | Deploying verified ERC20 contract to Ethereum Test Net (contract address to be provided for Node.JS application)                                                                                                                          | documents/ethereum_testnet_address_of_contract.txt                                  |
| 15%  | Providing functional Node.JS application to process token distribution file                                                                                                                                                               | src/tokenDistribution.js                                                            |
| 5%   | Providing access to github repo containing delivered assignment code                                                                                                                                                                      | documents/github_repo_url.txt                                                       |
| 10%  | Providing complete and clear readme.md instructions for application execution of token distribution                                                                                                                                       | readme.md                                                                           |
| 5%   | Providing Node.js application Docker container, along with clear instructions for building and executing distribution via Docker                                                                                                          | NiketanBlockChain-container.zip readme.md                       |
| 5%   | Making Docker container available on Docker Hub                                                                                                                                                                                           | documents/docker_hub_url.txt                                                        |
| 25%  | Providing 2-page report on process of development of contract and setting up of accounts across the platform                                                                                                                              | reports/NiketanBlockChain.docx                                            |
| 20%  | Providing 1-page report on the Use and Purpose of Smart Contracts as demonstrated in your project work. Provide your thoughts and insight into the impact of the ability to create tokens in this manner, including any ethical concerns. | reports/BlockChain.docx                                             |
| 5%   | 5-7 Min Pre-recorded Demonstration displaying the operation of the contract.                                                                                                                                                              | videos/https://youtu.be/gBFNbNTO-XM                                        |

# Ethereum Accounts

## Main Account

- [MA_01](https://ropsten.etherscan.io/address/0xEd31b9ee14BdE262a76b873C33a8253C7Cd28020) 0xEd31b9ee14BdE262a76b873C33a8253C7Cd28020

## Secondary Accounts

- [SA_01](https://ropsten.etherscan.io/address/0xc8AE2B352EA9C5E3De1e5E7835EaE6E8718b52DB) 0xc8AE2B352EA9C5E3De1e5E7835EaE6E8718b52DB
- [SA_02](https://ropsten.etherscan.io/address/0xF42B1B2D5D0A8395B76e659a654a8F78e1f685f9) 0xF42B1B2D5D0A8395B76e659a654a8F78e1f685f9

# ERC20 TRC Contract

[Token Contract Address](https://ropsten.etherscan.io/address/0xEd31b9ee14BdE262a76b873C33a8253C7Cd28020)
0xEd31b9ee14BdE262a76b873C33a8253C7Cd28020


### Parameter 1: Address[] (Pass account addresses as array)

```solidity
Sample Value:
["0x2F814cCb88A752F5ba274D76Fc65c2F9e5F264F0",
  "0xEa31b9ee14BdE262a76b873C33a8253C7Cd28020",
  "0xdE42B1B0575C85a4fae476a86D21b4BaCcF1F758",
  "0xcF250d3777BD6C86A302739C86058371997d6693",
  "0xeC1C18b1d9CD728C208113A6E1E7234425b1a29f"]
```

### Parameter 2: percentageAmount (%)

```solidity
Sample Value:
5
```

[Sample Transaction Result](https://ropsten.etherscan.io/tx/0x686696a83518e0e3085702d5cf183932bbf3a53a3ad533728573958abcaf2df1)
0x686696a83518e0e3085702d5cf183932bbf3a53a3ad533728573958abcaf2df1

# How to Execute TRC Token Distribution Node Application (Manual)

1. Download and install [Node](https://nodejs.org/en/download/)!
2. Go to BlockChain folder, make sure you can see package.json and type below command:
   ```npm
   npm i
   ```
3. Put the correct private key in src/tokenDistribution.js line **7**

   ```
   How to get the correct private key?

   Try to decode documents/encrypted_private_key.txt using Salad Chiper, https://cryptii.com/
   ```

4. Modify src/addresses.txt, make sure you put correct ETH accounts that you want to transfer, put line space between each of them
5. Make sure you still in BlockChain folder, type below command to run the application:
   ```npm
   node src/Distribution.js
   ```

# How to Execute TRC Token Distribution Node Application (Docker)

1. Put the correct private key in src/tokenDistribution.js line **7**

   ```
   How to get the correct private key?

   Try to documents/decode encrypted_private_key.txt using Salad Chiper, https://cryptii.com/
   ```

2. Modify src/addresses.txt, make sure you put correct ETH accounts that you want to transfer, put line space between each of them

3. Go to BlockChain folder, make sure you can see dockerfile and type below command:

   ```docker
   docker build -t BlockChain .
   ```

4. To run the docker, you can simply type below command:
   ```docker
   docker run BlockChain
   ```
5. If you lazy to build and configure, I have pushed defaulted value token distribution application as Docker image to Docker Hub, you can pull it and run using below command:
   ```docker
   docker pull BlockChain
   docker run BlockChain
   ```

# Closing

If you hit any issues or want to clarify something, don't hestitate to contact me at x20180837@student.ncirl.ie<br />
**Good luck and have fun!**
