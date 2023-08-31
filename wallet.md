---
layout: default
---

# Wallet

## Communicate with nodes

### Get balance
```https
METHOD getBalance
```
This returns the balance of user
#### Request
| Parameter | Type     | Description                     |
| :-------- | :------- | :-------------------------------- |
| `type` | `string` | **Required**. Method type |
| `data` | `string` | **Required**. Username of user |
#### Example response (JSON)
| Parameter | Type     | Value                     |
| :-------- | :------- | :-------------------------------- |
| `type` | `string` | dataResponse |
| `data` | `integer` | 650 |

### Submit transaction
```https
METHOD newTransaction
```
This sends a new transaction on behalf of the user to the network. The transaction is only valid with correct TSK.
#### Request
| Parameter | Type     | Description                     |
| :-------- | :------- | :-------------------------------- |
| `type` | `string` | **Required**. Method type |
| `data` | `string` | **Required**. Username of user |
#### Example response (JSON)
| Parameter | Type     | Value                     |
| :-------- | :------- | :-------------------------------- |
| `type` | `string` | dataResponse |
| `data` | `integer` | 650 |

