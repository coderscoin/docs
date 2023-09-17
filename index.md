---
layout: default
---

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Getting started

Welcome to CodersCoin official documentation. This website provides instructions for contributing to CodersCoin, as well as for running and configuring the node and mining software.

## Node

This is a guide on how to get a CodersCoin node up and running.

### 1. Installation

Navigate to the CodersCoin node Github repository and find the latest release on [this page](https://github.com/coderscoin/node/releases)! At the time of writing this documentation, the latest version is [2.0.0-beta](https://github.com/coderscoin/node/releases/tag/v2.0.0-beta).

Select the right verison for your system, download and unzip it! If you deploy from source code, run `npm install` in the project directory after unzipping the files! 

### 2. Setting up the node

In order for the CodersCoin node to function properly and for you to get the node reward, the node's data must be configured and added to the node explorer so that other nodes can discover it in the peer-to-peer network!

First, let's modify the `config.json` file! You need to replace the value of `runnerUser` with your Github username that you use as your CodersCoin wallet address. In my case, my username is petertill.

```json
{
    "nodeVersion": "v1.0.0",
    "nodeExplorer":"",
    "runnerUser": "petertill",
    "serverPort":"3000",
    "blockchainFile":"blockchain1.json",
    "transactionPoolFile":"transactions.json"
}
```

First, let's modify the `config.json` file! You need to replace the value of `runnerUser` with your Github username that you use as your CodersCoin wallet address. In my case, my username is petertill.

The next step is to add our node to the Node Explorer! The node explorer is nothing more than a json file stored in a [Github repository](https://github.com/coderscoin/nodexplorer) with the IP address, port, and username of all existing peers. 

In order to add your node, you must make the IP address and port where the CodersCoin node is running publicly available via port forwarding. If you can't handle port forwarding securely, it's safer to use ngrok.

If you have this, fork the node explorer repo and add the data of your node in the last line of the json file, then make a pull request!

```json
{"host": "191.0.1.255", "port": 3000, "user":"petertill"}
```

### 3. Using ngrok

> Your ngrok tcp url might change every time you start it, I have to figure something out for that.



### 4. Running it

If your pull request has been accepted, you are now part of CodersCoin's decentralized, peer-to-peer network! To run node, run the node index.js command from the project folder, or if you use an executable file, simply run it!



### Run a node

## Developers

> This is the collection of documentation for development and contribution purposes.
> The links below are for experienced users and developers only.

### Wallet

*   [Developer documentation](./wallet.html)

### Node

*   **SOON**

## Version support

### Mainnet

| version      | node    | wallet  | miner   |
|:-------------|:--------|:--------|:--------|
| v2.0.0       | &check; | &cross; | &cross; |

### Testnet

| version      | node    | wallet  | miner   |
|:-------------|:--------|:--------|:--------|
| v2.0.0       | &check; | &check; | &check; |


## NFTs

NFT metadata should be located in the ```data``` object. CodersCoin uses the transaction object for selling and transferring NFTs.

```json
"NFT":{
    "id": "140bc69a2d8e8d23d5264d3c33f7cffa583f2a4e2d64", 
    "metadata":{
        "title":"Dog NFT", 
        "description":"This is really cute", 
        "url":"https://mysite.com/assets/picture.jpg"
    }
}
```
