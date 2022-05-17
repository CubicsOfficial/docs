# Bridge

## Explanation
The Cubics Bridge enables users to swap Ether, BNB, or Cubics from Binance Smart Chain into native Cubics tokens and vice versa.

To create a bridge request, visit the Cubics network app and connect your wallets for the chains you want to exchange between. You will be able to specify your desired input amount, and you will see the approximate output amount. After you send the input transaction, it should take less than 5 minutes for the swap request to be completed, with a fee of around 2%.

## Intro
The Cubics bridge swaps between ETH/BNB/BSC CUBIC and native CUBIC tokens, with slippage of around 1.5% (plus regular liquidity slippage for amounts that impact liquidity). This process also works vice versa. The swap process takes about 5 minutes and is completely automated in both directions.

*Use Cases:  
Swapping supported assets from Ethereum (ETH) or Binance Smart Chain (BNB, CUBIC) to Cubics native tokens, Swapping native Cubics tokens into assets on Ethereum (ETH) or Binance Smart Chain (BNB, CUBIC)*

## Functionality
The user makes an input transfer to Cubics’s bridge wallet address on the chosen input chain. Cubics listens to all incoming transactions with a specifically formatted schema (the data/message field of transactions) and awaits a sufficient number of confirmations. After the transaction is confirmed, Cubics calculates the exchange rate based on swap size and its effect on liquidity to account for possible slippage. Slippage fees added on top of the base fee of 1.25%. Cubics then sends the output transfer on the chosen target chain to the wallet address connected by the user.

## Methods

### Create Bridge Request
Create a new bridge request.

**Requirements:** `ETH/BSC wallet`, `CUBIC wallet`  
**Outputs:** `Transfer on target chain`  
**Inputs:**  
`ETH/BSC public address`  
`CUBIC public address`  
`Swap amount`  
`Source-chain`  
`Target-chain`  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>