# Introduction to Vyper

Vyper is a Python-like programming language designed to write Ethereum smart contracts. It focuses on simplicity, security, and auditability, making it a great choice for developing smart contracts where security is a top priority.

## Why Vyper?

Vyper was developed as an alternative to Solidity, Ethereum's primary smart contract language, with the following goals:

- **Security**: Vyper aims to minimize security risks by eliminating complex features that can introduce vulnerabilities.
- **Simplicity**: The language is simple and minimalist, making smart contracts easier to read and audit.
- **Auditability**: The code is straightforward and easy to understand, making it easier for developers and auditors to verify the correctness of contracts.

## Key Features

Vyper has several key features that distinguish it from other smart contract languages:

- **Limited Data Types**: Vyper supports only essential data types, reducing the likelihood of errors.
- **No Modifiers**: Vyper eliminates the use of function modifiers, which can obscure the flow of control.
- **No Inheritance**: Vyper does not support class inheritance, making contract behavior more predictable.
- **Gas Optimization**: Vyper is designed to optimize gas usage, making contracts more cost-effective to deploy and interact with.

## Basic Vyper Syntax

Here's a simple example of a Vyper contract:

```python
# SimpleStorage.vy
# A simple smart contract to store and retrieve a value

stored_value: public(int128)

@external
def set_value(value: int128):
    self.stored_value = value

@view
@external
def get_value() -> int128:
    return self.stored_value

