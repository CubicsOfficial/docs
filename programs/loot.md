# Loot

## Explanation
Loot programs enable token creators to distribute their NFTs in a randomized way. A creator can set up a loot pool and deposit NFTs to it. Other users can then participate for the minimum required contribution and receive a random NFT based on the probability that the creator specified upon creation.

To participate in a loot pool, navigate to the loot pool page, connect your wallet, and click on “participate”. You will be prompted to send the minimum required amount of participation tokens to the pool, after which the program will determine whether you win an NFT. If you win, the NFT will be instantly transferred to your wallet.

To create a loot pool and distribute NFTs, visit the Cubics network app, connect your wallet and click on “new pool” under wallet actions. You will be able to specify a participation token, the participation amount, a win probability, and other details. Once the pool has been created, you can deposit NFTs to the pool, which will then be distributed to participants randomly once they enter. Once the pool has collected tokens from participants, you will be able to withdraw these tokens from the pool as earnings.

## Intro
Loot pools enable token-creators to promote their NFTs in a randomized fashion. Loot pools are equivalent to NFT drops. Users can participate by paying a certain fungible-token amount and receiving a random NFT with a certain probability.

*Use Case: Distributing or launching an NFT collection through randomized token distribution process*

## Functionality
The creator or owner of NFTs creates a loot pool and sets parameters such as the participation amount and win-probability. The creator deposits NFTs to the pool to be distributed. Participants can then enter by transferring the entry amount to receive a random NFT with a specific probability from the pool.

## Methods

### Transfer
Participate in the loot pool by transferring the required participation amount.

**Requirements:** `Positive NFT balance by pool`  
**Outputs:** `NFT transfer to sender based on win-probability`  
**Inputs:** `None`  

### Create
Create a new loot pool.

**Requirements:** `None`  
**Outputs:** `Loot pool`  
**Inputs:**  
`Token` - A fungible token to be used as participation token  
`Percentage` - Probability to win, between 0 and 1  
`MinAmount` - Participation amount  
`Expires` - Datetime when the loot pool expires  

### Deposit
Deposit an NFT as loot to the loot pool.

**Requirements:** `Pool creator`, `NFT ownership`  
**Outputs:** `NFT transfer from sender to pool`, `Deposit claim from pool to sender`  
**Inputs:**  
`Token` - NFT token to deposit to the loot pool  
`Unlocks` - Time until which the token will remain locked in the pool  

### Withdraw
Withdraw a previously deposited NFT, which has not been distributed yet.

**Requirements:** `Pool creator`, `Active deposit claim`  
**Outputs:** `NFT transfer from pool to sender`  
**Inputs:**  
`Claim` - Deposit claim hash  

### Clear
Clear all fungible-token proceeds held by the pool collected as entry amounts by participants by transferring them to the creator.

**Requirements:** `Pool creator`, `Token balance by pool`  
**Outputs:** `Token transfer from pool to pool creator`  
**Inputs:** `None`  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>