# Lock

## Explanation
Lock programs enable anyone to lock tokens for a specified period of time. Locks can also be used to lock tokens for others, for example, to distribute locked tokens to team members or investors. Once a lock is created, it can be unlocked only once the specified unlock period expires. Afterward, you or the beneficiary of the lock claim will be able to unlock their tokens.

To participate in an existing lock pool, visit the pool page and connect your wallet. You will be able to lock the tokens associated with the pool for your specified amount of time. Once the lock period expires, you or the beneficiary can unlock these tokens on the same page.

To create a lock pool for your token, visit the Cubics network app, connect your wallet and click on “new pool” under wallet actions. You will be able to specify the associated token and parameters such as minimum or maximum lock time and amount.

## Intro
Lock pools make it possible for anyone with a fungible-token balance to lock tokens for a specific time. Locks can be set to unlock after a particular date or be valid only before a date through an expiration mechanism. Furthermore, lock pools allow the transfer of lock claim ownership to other addresses.

*Use Cases:  
Locking fungible-tokens for someone (e.g. allocated for another entity as a form of vesting)  
Locking fungible-tokens until a specific datetime  
Locking fungible-tokens claimable after a particular date, and before an expiry date*

## Functionality
A lock pool is created for a particular token. Users can then use this pool to lock their tokens in exchange for a lock claim. This claim can then be redeemed after the locking period expires. Lock claims can be assigned to another address, allowing project creators to distribute tokens to others in a locked state.

## Methods

### Transfer
Create a new lock-claim for the token as specified by the pool.

**Requirements:** `Token balance`  
**Outputs:** `Token transfer from sender to pool`, `Lock claim from pool to sender`  
**Inputs:**  
`Amount` - Fungible-token amount to be locked  
`Address` - Address for which to lock the tokens  
`Unlocks` - Datetime from which the claim will be claimable  
`Expires` - Datetime at which the claim will expire and become non-claimable  

### Claim
Allows participants with a valid lock-claim to unlock tokens from the lock-pool.

**Requirements:** `Active lock claim`  
**Outputs:** `Token transfer from pool to sender`  
**Inputs:**  
`Claim` - Lock claim hash  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>