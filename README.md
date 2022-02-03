# React_BlockchainWeb3_App

Some files which you have to add yourself:

IN CLIENT:

# in utils folder, add (constants.js & Transactions.json):

# constants.js:
  import abi from "./Transactions.json";

  export const contractAddress = "0x054Bc75eC501...."; (value which you will get after running your deply.js file using hardhat)
  export const contractABI = abi.abi;

# Transactions.json:
  Copy this file from smart_contract-artifacts-contracts-Transactions.sol

IN SMART_CONTRACT:
# change hardhat.config.js: 
  
  require('@nomiclabs/hardhat-waffle');

  module.exports = {
    solidity: '0.8.0',
    networks: {
      ropsten: {
        url: 'https://eth-ropsten.alchemyapi.io/v2/....', (take url from alchemy.com)
        accounts: ['a85e1fda486818......'], (You'r main metamask account)
      },
    },
  };
