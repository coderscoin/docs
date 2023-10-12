---
layout: default
---
# CodersCoin Node

This is a guide on how to get a CodersCoin node up and running.

## 1. Installation

Navigate to the CodersCoin node [Github repository](https://github.com/coderscoin/node) and download the source code as a zip file or use ```git clone https://github.com/coderscoin/node.git```! 

After extracting the contents of the folder, run 
```
npm install
```
to install required packages.


### 2. Setting up the node

In order for the CodersCoin node to function properly and for you to get the node reward, the node's data must be configured in the ``config.json`` file so that other nodes can discover it in the peer-to-peer network!

First, let's modify the `config.json` file! You need to replace the value of `runnerUser` with your CodersCoin wallet address. In my case, my address is ``csc.6eeddf6f133ac189824ebb702a6b5e``.

```json
{
    "nodeVersion": "v2.5.0",
    "runnerUser": "csc.6eeddf6f133ac189824ebb702a6b5e", //Your address
    "serverIP":"localhost", //Your globally accessible ip/hostname
    "serverPort":"3000", //Your globally accessible port
    "blockchainFile":"blockchain1.json", //JSON file for blockchain storage
    "transactionPoolFile":"transactions.json", //JSON file for local transaction pool
    "seedPeer": {"host": "172.31.255.255", "port": 3001} //Seed node connection details
}
```
In order to add your node, you must make the IP address and port where the CodersCoin node is running publicly available via port forwarding. If you can't handle port forwarding securely, it's safer to use ngrok.

You may need to replace the ``seedPeer`` that introduces you to the network if it is offline. You can find a list of seed nodes at [this JSON file](https://github.com/coderscoin/seednodes/blob/main/peers.json).

You can also add your own machine as a seed node by creating a pull request!

### 3. Using ngrok

> Your ngrok tcp url might change every time you start it, I have to figure something out for that.



### 4. Running it

You are now part of CodersCoin's decentralized, peer-to-peer network! To run the node script, run the 
```
node index.js
```
command from the project folder!

