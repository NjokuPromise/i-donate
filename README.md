# i-donate: A Charitable Donation DApp on Cartesi

## Overview

i-donate is a decentralized application (DApp) built on the Cartesi platform. It facilitates the creation of accounts, starting charities, and making donations to registered charities. The DApp leverages Ethereum for handling transactions and offers a structured interface to manage charitable donations securely.

## Features

- **Account Management**: Create and manage user accounts.
- **Charity Registration**: Register new charities with metadata.
- **Donations**: Make donations to registered charities.
- **Transaction Management**: Track pending donations.
- **Inspection Endpoints**: Retrieve details for accounts, charities, and pending transactions.

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/NjokuPromise/i-donate.git
   cd i-donate
   ```

2. **Install Dependencies**:
   Ensure you have Python installed. Then, install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the DApp**:
   ```bash
   python main.py
   ```

## API Endpoints

### Advance Commands

- **CREATE_ACCOUNT**: Creates a new account.
- **MAKE_DONATION**: Creates a pending donation transaction.
- **START_CHARITY**: Registers a new charity.

### Inspection Endpoints

- **/account/:private_key**: Retrieve account details.
- **/charity/:address**: Retrieve charity details.
- **/pending_transactions/:address**: Retrieve pending donation transactions for an account.

## Example Usage

- **Creating an Account**:

  ```json
  {
    "command": "CREATE_ACCOUNT",
    "data": {
      "address": "0x123...",
      "name": "John Doe",
      "meta": "Some metadata"
    }
  }
  ```

- **Making a Donation**:

  ```json
  {
    "command": "MAKE_DONATION",
    "data": {
      "private_key": "user-private-key",
      "charity_address": "0xabc...",
      "amount": 100
    }
  }
  ```

- **Starting a Charity**:
  ```json
  {
    "command": "START_CHARITY",
    "data": {
      "address": "0xdef...",
      "name": "Charity Name",
      "meta": "Charity metadata"
    }
  }
  ```

## Logging

The application uses Python's `logging` module to output debug information, making it easier to track the internal state and troubleshoot issues.
