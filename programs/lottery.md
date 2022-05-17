# Lottery

## Explanation
Lotteries enable the distribution of fungible and non-fungible tokens in a randomized way. Users can participate by sending the minimum required CUBIC amount to the lottery pool. After the lottery expires, winners can claim from the prize pool. In the case of an NFT lottery, the lottery automatically distributes its prize to one random winner.

To participate in a lottery pool, open the lottery pool page, connect your wallet and click on participate. You will be requested to transfer the minimum required CUBIC amount to enter, in exchange for a participation claim. After the lottery pool expires or reaches its maximum number of participants, you will be able to claim your ticket and you will be awarded from the prize pool with the probability as determined by the pool upon resolution.

To create a lottery, visit the Cubics network app, connect your wallet and select “new pool” under wallet actions. You will be able to specify the associated prize token and values such as minimum participation amount, number of winners, or required CUBIC balance of eligible users. Once the pool has been created, you need to deposit the prize tokens to the pool, after which users can participate until the pool expires and resolves.

## Intro
Lottery pools allow the distribution of fungible or non-fungible tokens in a randomized way. Lotteries can be based on specific criteria, such as a minimum token amount that someone must hold to participate or require a minimum amount to enter. After a lottery expires, it can be resolved to automatically distribute the NFT or make the fungible tokens claimable for winning participants.

*Use Cases:  
Distributing an NFT through a randomized mechanism and a single winner  
Distributing fungible-tokens through a randomized mechanism*

## Functionality
A lottery pool can promote a fungible or single non-fungible token to participants, who can enter to win with a probability dependent on the number of entries. After creating the lottery pool, the creator must deposit the fungible tokens or a single NFT. Once the deposit is complete, any user can participate, either for free or the minimum amount required by the pool. Furthermore, pools can set a minimum amount of CUBIC that a user needs to hold to be eligible to participate. Requiring a minimum amount of CUBIC to participate improves incentives and prevents dishonest entries (especially if the lottery pool is sponsored).

After the lottery pool expires, the resolution call automatically transfers the NFT to a single winner chosen from all participants. If the lottery is promoting a fungible token, winners (based on the pools’ probability) can claim their fungible-token rewards using their claimable ticket.

## Methods

### Transfer
Transfer the entry amount to participate in the lottery.

**Requirements:** `Token balance`, `CUBIC balance`  
**Outputs:** `CUBIC transfer from sender to pool`, `Transfer claim from pool to sender`  
**Inputs:** `None`  

### Claim
Claim a lottery ticket, and receive the pool token with a certain probability.

**Requirements:** `Active transfer claim`  
**Outputs:** `NFT or token with a probability as specified by the pool`  
**Inputs:**  
`Claim` - Claim hash  

### Resolve
Resolve a lottery pool and determine the winner of an NFT lottery.

**Requirements:** `NFT lottery`  
**Outputs:** `NFT transfer from pool to random participant`  
**Inputs:** `None`  

### Create
Create a lottery pool for fungible tokens or a single non-fungible token.

**Requirements:** `None`  
**Outputs:** `Lottery pool`  
**Inputs:**  
`Token` - The token which is to be promoted  
`MinAmount` - Participation amount  
`TokenTarget` - Amount of pool tokens that someone must hold to participate  
`CubicsTarget` - Amount of CUBIC, that someone must hold to participate  
`TransfersLimit` - Maximum amount of participants  
`ClaimsLimit` - Maximum number of winners  
`Expires` - Datetime when lottery naturally expires   

### Deposit
Allows the creator to deposit the pool token.

**Requirements:** `Pool creator`  
**Outputs:** `Token transfer from sender to pool`, `Deposit claim from pool to sender`  
**Inputs:**  
`Amount` - Amount in case of a fungible-token lottery  
`Unlocks` - Datetime when the claim unlocks  

### Withdraw
Allows the creator to withdraw a previously deposited pool token.

**Requirements:** `Pool creator`, `Active deposit claim`  
**Outputs:** `Token transfer from pool to sender`  
**Inputs:**  
`Claim` - Deposit claim hash  

### Close
The creator can close the lottery before expiration. If there are participants, the creator can only withdraw the unclaimable share.

**Requirements:** `Pool creator`  
**Outputs:** `None`  
**Inputs:** `None`  

### Clear
Allows the creator to clear CUBIC earnings collected by the lottery pool if the participation amount is positive.

**Requirements:** `Pool creator`, `CUBIC balance by pool`  
**Outputs:** `CUBIC transfer from pool to pool creator`  
**Inputs:** `None`  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>