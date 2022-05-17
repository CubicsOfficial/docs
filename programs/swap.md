# Swap

## Explanation
Swap pools are automatically created for every fungible token that is minted on Cubics. Swaps enable anyone to exchange CUBIC for tokens and vice versa. This exchange process is fully decentralized, and prices are automatically determined based on the available CUBIC and token liquidity.

To trade a token, visit the swap pool page of a token and connect your wallet. You will be able to select the amount you would like to swap, as well as the input token. Once you confirm your transaction, you will receive the output token within a short period of time.

## Intro
Swap pools are automatically created for every fungible token that is minted. These allow participants to swap tokens against CUBIC and vice versa in a decentralized way. The price is based on the liquidity that token creators and participants can contribute, and the trades that affect the liquidity.

*Use Case: Decentralized exchange mechanism for fungible tokens*

## Functionality
A swap pool is automatically created with the creation of every fungible token. Creators can add liquidity via a launch pool, or directly by depositing the pool tokens and CUBIC. The amount of deposited liquidity determines the price, which is determined by dividing the number of tokens available as liquidity by the amount of CUBIC available as liquidity. Participants can swap CUBIC for tokens or tokens for CUBIC. Transfers in and out are entirely handled by the program in an automated way, charging 0.25% commission on every trade and automatically adding 1% of the trade value to the pools’ liquidity.

## Methods

### Transfer
Swap tokens into CUBIC or CUBIC into tokens at the current exchange rate.

**Requirements:** `Pool liquidity`  
**Outputs:** `Transfer from sender to pool`, `Transfer from pool to sender`  
**Inputs:**  
`Token` - CUBIC or the pool-token, to use as input token  
`Amount` - Number of tokens to swap  

### Deposit
Deposit CUBIC and tokens to liquidity at a specific rate.

**Requirements:** `CUBIC balance`, `Token balance`  
**Outputs:** `CUBIC transfer from sender to pool`, `Token transfer from sender to pool`, `Liquidity deposit claim from pool to sender`  
**Inputs:**  
`TokenAmount` - Amount of tokens to deposit  
`CubicsAmount` - Amount of CUBIC to deposit  
`Unlocks` - Datetime when the deposit claim shall unlock  

### Withdraw
Allows withdrawing previously deposited liquidity tokens adjusted for the new liquidity rate.

**Requirements:** `Active liquidity deposit claim`  
**Outputs:** `CUBIC transfer from pool to sender`, `Token transfer from pool to sender`  
**Inputs:**  
`Claim` - Deposit claim hash  
`Percentage` - Percentage between 0-1 to withdraw  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>