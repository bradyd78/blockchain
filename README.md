# Blockchain Project

## Project Description

**blockchain** is a simple blockchain implementation in Python, inspired by the tutorial ["Learn Blockchains by Building One"](https://hackernoon.com/learn-blockchains-by-building-one-117428612f46).

This project demonstrates:
- A basic blockchain data structure
- Transaction recording and mining (proof-of-work)
- A RESTful API using Flask for interacting with the blockchain

It is ideal for learning blockchain fundamentals and experimenting with a working prototype.

---

## Getting Started

### Prerequisites

- Python 3.x
- Flask (`pip install flask`)

---

## Running the Server

Start the blockchain server with:

```sh
python blockchain.py
```

The server will run at `http://127.0.0.1:5000/`.

---

## API Usage & Testing

You can interact with the blockchain using cURL or Postman.

### 1. Mine a Block

Mine a new block:

```
GET http://localhost:5000/mine
```

---

### 2. Create a Transaction

Send a POST request to create a new transaction:

```
POST http://localhost:5000/transactions/new
Content-Type: application/json

{
  "sender": "d4ee26eee15148ee92c6cd394edd974e",
  "recipient": "someone-other-address",
  "amount": 5
}
```

Using cURL:

```sh
curl -X POST -H "Content-Type: application/json" -d '{
  "sender": "d4ee26eee15148ee92c6cd394edd974e",
  "recipient": "someone-other-address",
  "amount": 5
}' "http://localhost:5000/transactions/new"
```

---

### 3. View the Blockchain

Get the full blockchain and its length:

```
GET http://localhost:5000/chain
```

---

### 4. View Blockchain Stats

See chain length, pending and total transactions, and participant addresses:

```
GET http://localhost:5000/census
```

---

## Summary

- Run `python blockchain.py` to launch the server.
- Use `/mine`, `/transactions/new`, `/chain`, and `/census` endpoints for blockchain operations.
- Interact using Postman or cURL for hands-on learning.

---
