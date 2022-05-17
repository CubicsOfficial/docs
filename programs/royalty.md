# Royalty

## Explanation
Royalty programs enable NFT holders to earn passive income by claiming royalties from it. Creators set up a pool with token rewards for all or a subset of NFTs, and any user holding an eligible NFT can claim royalties simply for holding the NFT.

To claim royalties, visit the royalty pool page, connect your wallet and click on “claim”. You will automatically receive a payout from the pool, as long as you hold an NFT that is eligible. Rewards accumulate day by day, and you receive daily rewards that have accumulated since your last claim date.

To create a royalty pool and reward NFT holders with passive income, visit the Cubics network app, connect your wallet and click on “new pool” under wallet actions. You will be able to specify the associated reward token as well as a daily reward rate. Once the pool has been created, you can deposit reward tokens to it, so that other users can claim these tokens as royalties.

## Intro
Royalty pools allow NFT creators to allocate a particular token for royalty payouts of NFT holders. Anyone who owns an NFT specified by a royalty pool can claim royalties based on the holding duration.

*Use Cases:  
Reward NFT holders based on the length of holding a certain NFT
Pay a passive income/royalties for anything in the physical or virtual reality, represented by an NFT*

## Functionality
A creator creates a royalty pool and specifies candidates and a linear pay-out rate of rewards. After depositing rewards, any owner of NFTs created by the creator (and as determined by the royalty pool) can then periodically claim royalties from the pool. Royalties accumulate every day until a claim is made (claims reset the daily counter).

## Methods

### Claim
Claim royalties for an NFT created by the royalty-pool creator, depending on the length of holding the NFT.

**Requirements:** `Claim answer in pool candidates, or no candidates`  
**Outputs:** `Royalty transfer from pool to sender`  
**Inputs:**  
`Token` - Token address  

### Create
Create a royalty pool while specifying the eligible NFT candidates and a daily royalty rate.

**Requirements:** `None`  
**Outputs:** `Royalty pool`  
**Inputs:**  
`Token` - A fungible token that is used as reward payout  
`Candidates` - A list of NFT candidates, or empty if all NFTs by the creator should be eligible  
`Rate` - Amount of pool-tokens that is paid for every day of holding the NFT  
`Expires` - Datetime when the royalty pool is no longer valid  

### Deposit
Deposit a certain amount of pool-tokens available as reward payouts for NFT holders.

**Requirements:** `Pool creator`  
**Outputs:** `Reward token transfer from sender to pool`, `Deposit claim from pool to sender`  
**Inputs:**  
`Amount` - Reward amount to be deposited  
`Unlocks` - Datetime when the deposit claim can be withdrawn  

### Withdraw
Withdraw previously deposited reward tokens (partially if rewards have been claimed already).

**Requirements:** `Pool creator`, `Active deposit claim`, `Token balance by pool`  
**Outputs:** `Token transfer from pool to sender`  
**Inputs:**  
`Claim` - Deposit claim hash  

### Close
The creator can close a royalty pool at any time, making it impossible to claim additional royalties.

**Requirements:** `Pool creator`  
**Outputs:** `None`  
**Inputs:** `None`  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>