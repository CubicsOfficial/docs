# Claim

## Explanation
Claims represent a promise or contract that is made between two parties. The issuing party issues a claim to someone who then holds the claim and has the right to redeem that claim based on the terms specified by the claim issuer. Terms for a claim can be the length of time, amount, or even a custom-written agreement.

When a person or entity issues a claim, the ​​fulfillment of the claim, even upon redemption and valid terms, is not guaranteed. Any person who issues a claim to someone is held publicly accountable with their integrity and trust, however, they might fail to fulfill the promise made.

On the other hand, claims issued by pools that execute verifiable contracts are always guaranteed to resolve successfully, as long as the claim conditions are met, and the pool owns sufficient tokens to resolve the claim.

To create a claim, visit the Cubics network app, connect your wallet by clicking on the “connect” button on the top right and selecting “new claim”. You will be able to assign an owner for the claim, setting an associated claim token as well as claim amounts. You will be able to specify when the claim should be able to unlock or when it should expire.

Most commonly, claims represent tickets for something that you contribute to a pool. For example, you might submit a vote to a voting pool or a bid to an auction pool. Alternatively, you might deposit tokens to a swap-liquidity or staking pool or participate in a lottery pool. In all of these cases, you receive a claim, which enables you to redeem it at a later point in time, based on the pools’ resolution mechanism.

## Intro
Claims represent a promise or contract that is made between two parties. A claim creator issues a claim to someone representing an option that can be redeemed based on specified terms such as timeframe or amount. The claim owner can redeem the claim once the condition of the claim is met. The fulfillment of promises made by claims is not guaranteed and is dependent on the issuers’ integrity and trust. However, if a pool with a verifiable program issues the claim, the claim resolution can be guaranteed through code.

*Use Cases:  
Claims between two users (credit claims, ownership claims, contracts, promises)  
Claims between a pool and a user (liquidity claim, deposit claim, vote claim, lottery ticket claim, etc.)*

## Functionality
A claim creator creates a claim based on a specific agreement and issues it to a user who has the right to claim once the conditions are met. Most frequently, pools use claims as a ticket to the user, who can redeem the ticket. Created claims can be updated by the creator at any time until resolution. Claim creators can also mark claims as resolved, at which point the claim becomes settled and cannot be updated any longer. Owned claims can be transferred as long as they are not frozen.

## Methods

### Create
Enables a pool or user to issue a claim to someone.

**Requirements:** `Claim token balance/ownership`  
**Outputs:** `Claim assigned to specified owner`  
**Inputs:**  
`Owner` - Holder who receives the claim  
`Token` - Claimable token  
`TokenAmount` - Claimable token amount  
`CubicsAmount` - Claimable Cubics amount  
`Expires` - Expiry date for the claim  
`Unlocks` - Date at which the claim becomes claimable  
`Frozen` - Forbids claim transfers, if set to true  
`Category` - Claim category  
`Meta` - Custom metadata as a JSON object  
`Answer` - Claimed answer  
`Number` - Claimed number  

### Transfer
Enables the claim owner to transfer claim ownership.

**Requirements:** `Unfrozen claim`  
**Outputs:** `None`  
**Inputs:**  
`Claim` - Claim hash  
`To` - To address  

### Update
Enables the claim creator to update specific claim values.

**Requirements:** `Claim creator`  
**Outputs:** `None`  
**Inputs:**  
`Claim` - Claim hash  
`TokenAmount` - Claimable token amount  
`CubicsAmount` - Claimable Cubics amount  
`Expires` - Expiry date for the claim  
`Unlocks` - Date at which the claim becomes claimable  
`Frozen` - Forbids claim transfers, if set to true  
`Category` - Claim category  
`Meta` - Custom metadata as a JSON object  
`Answer` - Claimed answer  
`Number` - Claimed number  

### Resolve
Enables the claim creator to close a claim and tag it as resolved.

**Requirements:** `Claim creator`  
**Outputs:** `None`  
**Inputs:**  
`Claim` - Claim hash  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>