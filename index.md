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

[Run a node](./node.html)


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
