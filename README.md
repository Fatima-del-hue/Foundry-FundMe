#About 
A decentralized crowdfunding smart contract built using Foundry and Chainlink.
This project allows users to fund the contract owner in ETH, with each contribution valued in USD using Chainlink Price Feeds.
If a donation doesn’t meet the minimum USD threshold, it’s rejected.
The contract tracks all funders, making it easy to reward or refund contributors later.


#Getting Started
This section will help you set up the project locally so you can build, test, and deploy the Fund Me smart contract yourself.
Whether you’re new to Foundry or already familiar with Solidity, these steps will get you running quickly and confidently.


#Requirements
Before you begin, make sure you have the following installed:
-Foundry
 (includes forge and cast)
-Git
-Node.js
 (optional, for managing dependencies or scripts)
-VS Code
-An Alchemy or Infura RPC URL for Sepolia or Mainnet
-A private key for a wallet with testnet ETH (do not use your real wallet)
(Optional) Etherscan API Key for contract verification



#QuickStart
Clone the repository and install dependencies:

git clone https://github.com/<your-username>/Foundry-FundMe.git
cd Foundry-FundMe
forge install


Build the project:
forge build


Run all tests:
forge test -vvv


To deploy on Sepolia, make sure your .env file is set up, then:
make deploy-sepolia


After deployment, you can verify the contract using:
forge verify-contract <DEPLOYED_CONTRACT_ADDRESS> <CONTRACT_PATH>:FundMe --chain sepolia
