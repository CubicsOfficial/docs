# Allowance

## Explanation
Allowances allow other people to spend your fungible tokens, up to a specified amount. You can create an allowance by visiting the Cubics network app and connecting your wallet by clicking on the “connect” button in the top right corner. After you’ve connected your wallet, you can select it and choose “new allowance”. Here, you can simply define the spender, the fungible token, and the amount which the spender-address should be able to spend on your behalf.

To spend an allowance that has been granted to you, connect your wallet and select “new transfer” under wallet actions. Fill in the required transfer fields such as to-address, token, and amount. At the bottom of the form, you will find an optional from-field, which you can use to specify the grantee address. This should be the public address of the person or entity who created an allowance for you. By specifying a from-address, your transfer will be sent on their behalf and will withdraw tokens from their wallet and send them to the specified recipient.

## Intro
An allowance can be given to another address, which is then allowed to spend a particular fungible token amount on behalf of the creator.

*Use Case: Allowing someone to spend funds on your behalf*

## Functionality
A user sets an allowance, granting another spender the right to spend a particular fungible token for a certain amount. The spender then can create transfers by specifying the from address to be the address that granted the allowance. The allowance creator can increase and decrease their given allowances at any time. The spender can make transfers until the creator’s allowance is depleted or adjusted to zero.

## Methods

### Update Allowance
Allows a spender to spend your tokens for the specified amount.

**Requirements:** `Token balance`  
**Outputs:** `Allowance to spend`  
**Inputs:**  
`Spender` - Public address of the spender  
`Token` - Fungible-token address  
`Amount` - Allowance amount  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>