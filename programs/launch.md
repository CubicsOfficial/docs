# Launch

## Explanation
Launch programs allow creators to raise funds for a project by offering fungible tokens in exchange for CUBIC. After a launch has been created, users can participate in it until the launch completes and resolves. Afterward, users can claim the project tokens if the launch was successful, or their initial CUBIC contribution if the launch didn’t reach the minimum fundraising target.

To participate in a launch, visit the launch pool on the Cubics network app and click on “participate”. You will be able to specify a CUBIC amount that you would like to contribute, in exchange for tokens that the pool promotes. After the launch completes, you will be able to claim your tokens through the same pool page.

To create a launch pool, visit the Cubics network app, connect your wallet and click on “new pool” under wallet actions. You will be able to set your project token, the fundraising limit, target, as well as other configurations. Afterward, you can deposit tokens to the pool which will determine the launch rate. Keep in mind that half of the launch tokens are allocated for participants, while the other half is allocated for the swap pool liquidity of the associated token.

## Intro
Launch pools allow creators to raise funds for a project by offering fungible tokens representing the project in exchange for CUBIC. Launch pools have a fixed rate of raising funds and a target (minimum) and limit (maximum) CUBIC amount. A successful launch pool (target amount reached before closure/expiry) automatically handles the liquidity deposit to the fungible token swap pool. Anyone who participated in the launch pool can then claim fungible tokens or recover their initial contribution if the launch didn’t raise the target amount.

*Use Case: Raise funds for a project and automatically distribute raised funds to liquidity and/or creators.*

## Functionality
A fungible-token owner creates a launch pool for a fungible token and shares it with users who can participate by contributing CUBIC tokens. Pool creators can decide how many tokens they want to offer and how much they want to raise as a minimum and maximum amount. Once a launch expires or closes, participants can claim back either tokens (upon success) or their CUBIC contribution (upon failure). Since the pool automatically handles the liquidity deposit, successfully resolved launches are automatically tradeable at the token swap pool.

## Methods

### Transfer
Transfer CUBIC to the launch pool to participate.

**Requirements:** `Active pool`  
**Outputs:** `CUBIC transfer from sender to pool`, `Transfer claim from pool to sender`  
**Inputs:**  
`Amount` - CUBIC contribution amount  

### Claim
Claim tokens upon success or CUBIC contribution upon failure.

**Requirements:** `Concluded pool`, `Transfer claim`  
**Outputs:** `Token transfer from pool to sender on pool success`, `CUBIC transfer from pool to sender on pool failure`  
**Inputs:**  
`Claim` - Claim hash    

### Resolve
Resolve launch pool after expiry or if creator manually closed pool.

**Requirements:** `Pool CubicsBalance >= CubicsTarget`  
**Outputs:** `Liquidity transfer from launch pool to swap pool`, `Funds transfer from launch pool to pool creator`  
**Inputs:**  
`Token` - Pool token  

### Create
Create a launch pool for a fungible token.

**Requirements:** `Token balance`  
**Outputs:** `Launch pool`  
**Inputs:**  
`Token` - Token to launch  
`CubicsTarget` - Minimum CUBIC target  
`CubicsLimit` - Maximum CUBIC limit  
`Percentage` - Percentage for liquidity vs. creator  
`TransfersLimit` - Maximum number of participants  
`Expires` - Datetime of expiry  

### Deposit
Deposit the fungible tokens and automatically determine the swap rate, based on 50% of the deposited amount allocated for swaps, 50% allocated for liquidity.

**Requirements:** `Pool creator`  
**Outputs:** `Token transfer from sender to pool`, `Deposit claim from pool to sender`    
**Inputs:**  
`Amount` - Amount to be deposited  
`Unlocks` - Unlocks datetime for claim  

### Withdraw
Withdraw previously deposited tokens, or remainder for a closed launch.

**Requirements:** `Pool creator`, `Token balance in the pool`  
**Outputs:** `Token transfer from pool to sender`  
**Inputs:**  
`Claim` - Claim hash  

### Close
Creators can close the launch pool manually before expiry.

**Requirements:** `Pool creator`  
**Outputs:** `None`  
**Inputs:** `None`  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>