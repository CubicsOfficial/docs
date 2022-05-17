# Lending

## Explanation
Lending enables users to borrow fungible tokens against CUBIC collateral. Lending promotes efficient markets as users can borrow tokens to speculate on the decline of a token price. Other use cases for lending might include paying or resolving a claim without owning the token. Lenders can earn attractive interest rates for tokens that they make available for borrowing.

To borrow tokens, visit the lending pool on the Cubics network app, connect your wallet and click on borrow. You will be prompted to specify a collateralization value, depending on the minimum collateralization required by the pool. This value determines the amount of tokens that you will receive in return for the CUBIC amount that you specify.

You can keep borrowed tokens indefinitely as long as your collateralization remains above 75% of the minimum. You can return your tokens using the same lending pool that you’ve borrowed from while being charged an interest rate based on the borrowed duration. In case your collateralization drops below 75% of the pools’ minimum, other users can liquidate your lending claim, and your CUBIC collateral will be used to cover open interest, penalty fees, and the borrowed token amount. The liquidated fees will be used to reimburse lenders.

To lend tokens to others, visit the lending pool and select deposit from the dropdown. You will be able to deposit the associated pool tokens, and you will earn interest from all collected CUBIC rewards proportionally that are collected while your tokens remain deposited.

## Intro
Lending pools allow users to borrow tokens against CUBIC collateral. Lending pools allow “short selling” a token or resolving claims without owning the token. At the same time, it enables lenders to earn interest by making their tokens available for borrowers.

*Use Cases:  
Short-selling a borrowed token based on the assumption that tokens can be purchased back at a lower price (contributing to more efficient markets)  
Earning interest by lending out fungible tokens to borrowers*

## Functionality
A lending pool is created with a certain collateralization and interest rate. Lenders deposit tokens into the lending pool. Borrowers can then use it to borrow tokens while specifying the desired collateral. As long as the collateralization is kept above the minimum, users can keep tokens for as long as they wish and pay the respective interest rate upon settlement. If, however, the collateralization rate falls below the minimum, any user can liquidate the borrower's claim, which applies penalties equivalent to a one-year interest rate to the borrower's collateral.

All collected funds, via interest rate paid by the borrower, including liquidations, are collected and proportionally divided between lenders based on lending duration and lending amount. Lending pools make it possible for lenders to earn a steady and predictable interest rate.

## Methods

### Transfer
Lend tokens from the lending pool at certain collateralization.

**Requirements:** `Collateralization >= Min. collateralization`  
**Outputs:** `CUBIC transfer from sender to pool`, `Token transfer from pool to sender`  
**Inputs:**  
`Token` - Pool token (token to borrow)  
`Collateralization` - Desired collateralization rate  
`Amount` - CUBIC amount to be transferred as collateral  

### Settle
Return previously lent tokens while paying an interest rate based on the rate specified by the pool and the lending duration.

**Requirements:** `None`  
**Outputs:** `Token transfer from sender to pool`, `CUBIC transfer from pool to sender`  
**Inputs:**  
`Claim` - Claim hash  

### Liquidate
Liquidate someone’s claim that has dropped below 75% of the minimum collateralization required by the pool.

**Requirements:** `Claim collateralization < 0.75 * min. collateralization`  
**Outputs:** `CUBIC transfer from pool to borrower for remaining collateral`, `CUBIC transfer from pool to liquidator for finders reward`  
**Inputs:**  
`Claim` - Claim hash 
`Token` - Pool token  

### Deposit
Deposit tokens as specified by the pool to earn a specific interest rate.

**Requirements:** `None`  
**Outputs:** `Token transfer from sender to pool`, `Deposit claim from pool to sender`  
**Inputs:**  
`Amount` - The deposited amount  
`Unlocks` - A datetime when the deposit claim can be redeemed  

### Withdraw
Withdraw tokens that have been deposited previously to the lending pool.

**Requirements:** `Active deposit claim`  
**Outputs:** `Token transfer from pool to sender`, `CUBIC transfer from pool to sender for interest earned`  
**Inputs:**  
`Claim` - Deposit claim hash  
`Token` - Pool token  
`Percentage` - Percentage to withdraw  

### Create
Create a lending pool for a fungible token.

**Requirements:** `None`  
**Outputs:** `Lending pool`  
**Inputs:**  
`Token` - Token to lend/borrow  
`Percentage` - Collateralization rate  
`Rate` - Annual interest rate  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>