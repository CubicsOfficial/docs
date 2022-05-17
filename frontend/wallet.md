# Wallet

## Explanation
The Cubics Wallet enables users to create a managed or self-managed wallet on Cubics. Wallets can be used to send and receive transfers, mint and hold tokens, or participate in pools. Wallets on Cubics are available in two options.

The self-managed wallet generates a private and public key pair that you have to store securely. The 3rd party managed wallet option handles private keys for you and allows you to access your wallet with a username and password.

To create a new Cubics wallet, visit the Cubics network app and click on “connect wallet” in the top right corner. You will be prompted to choose between the managed or self-managed option to create a new wallet. To connect an existing wallet, choose your desired method and enter your private key if you have a self-managed wallet or your account username and password if you choose the managed wallet option.

Once your wallet is connected, you can click on it to perform various actions, such as viewing your address page, backing up your keys, or creating transactions.

## Intro
Cubics’s wallet allows users to create and manage their CUBIC blockchain wallets, either by managing keys yourself or letting a 3rd party provider (currently Cubics foundation) manage keys for you.

*Use Cases:  
Create a new self-managed or managed Cubics wallet  
Connect an existing self-managed or managed Cubics wallet*

## Functionality
Users need a wallet to interact with the Cubics blockchain. Users can create a key pair (public key/private key) or let a provider manage this keypair for them (using a more memorable account and secret). Once a wallet is created through the self-managed or managed option, it can be connected to Cubics’s apps, as long as the owner has access to the private key or account and secret (in the case of managed keys).

## Methods

### Create Self-Managed
Create a new CUBIC blockchain key pair.

**Requirements:** `None`  
**Outputs:** `Public key`, `Private key`  
**Inputs:** `None`  

### Create Managed
Create a managed wallet.

**Requirements:** `None`  
**Outputs:** `Public key`  
**Inputs:**  
`Account` - Memorable account name, for example, email, phone number, or username  
`Secret` - Memorable password

### Connect Self-Managed
Connect a self-managed wallet.

**Requirements:** `Private key`  
**Outputs:** `None`  
**Inputs:** `None`  

### Connect Managed
Connect a managed wallet.

**Requirements:** `Account name`, `Account secret`  
**Outputs:** `None`  
**Inputs:** `None`  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>