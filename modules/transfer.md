# Transfer

## Explanation
A transfer enables anyone to transfer a token, whether fungible or non-fungible, to someone else’s wallet. Fungible token transfers always credit and debit balances with an amount, while non-fungible token transfers simply change the ownership address of the NFT.

To create a transfer, visit the Cubics network app and click on “connect wallet” in the top right corner. Afterward, you will be able to select “new transfer” under wallet actions and submit transfer details such as recipient, token, and optionally a token amount if you wish to transfer a fungible token. Transfers can include a message for the recipient, or specify a from-address to make use of an allowance.

## Intro
A transfer allows the transfer of fungible and non-fungible tokens between addresses.

*Use Cases:  
Transferring an amount of a fungible token  
Transferring a non-fungible token*

## Functionality
A user with a certain fungible-token balance can transfer all or parts of the balance to another address. Additionally, a user who owns a particular non-fungible token can create a transfer to assign ownership to another address.

## Methods

### Create
Create a new fungible or non-fungible token transfer.

**Requirements:** `Token balance/ownership`  
**Outputs:** `Token transfer from sender to recipient`  
**Inputs:**  
`To` - To address for the transfer  
`Token` - Token to be transferred  
`Amount` - Transfer amount for FT, empty if NFT  
`From` - From address in case of allowance  
`Message` - Custom transfer message  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>