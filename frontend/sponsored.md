# Sponsored

## Explanation
Cubics enables users to sponsor an address and delegate network fees. Sponsored addresses automatically reimburse other users who send transfers to it. This works exceptionally well with pools that would like to enable free transactions. Think about a swap pool without fees or a voting pool where anyone can vote without dealing with Cubics tokens. Similarly, you can sponsor your address and allow others to send you transfers without a fee.

To sponsor an address, visit the Cubics network app and connect your wallet by clicking “connect wallet” on the top right. Under wallet actions, select “new transfer” and enter the address you would like to sponsor in the to-field. Under token, select “Cubics Sponsored,” which will be debited as Cubics and credited as sponsored Cubics to the recipients’ balance. Just keep in mind that sponsored Cubics balances cannot be transferred, even if you sponsor your own address.

## Intro
Cubics enables users to transfer a sponsored balance to addresses or pools, so other users interacting with these resources can do so without paying network fees.

*Use Cases:  
Recipient sponsoring incoming transfers to their address  
Pool sponsoring incoming transfers and enabling participation without owning CUBIC  
Project creators who would like to encourage participation in particular pools*

## Functionality
A user transfers sponsored CUBIC tokens to an address or pool. The transferred token is specified as sponsored CUBIC and is automatically swapped from the users' CUBIC balance into sponsored CUBIC and credited to the resource. Other users who interact with the sponsored resource won't be charged any fees until the sponsored balance of the resource is depleted.

## Methods

### Create
Swaps the users' owned CUBIC into sponsored CUBIC. Sponsored CUBIC cannot be withdrawn.

**Requirements:** `CUBIC balance`  
**Outputs:** `Sponsored CUBIC transfer from sender to recipient`  
**Inputs:**  
`To` - Recipient resource to be sponsored  
`Token` - Must be specified as 1111111111111111111111111sponsored  
`Amount` - Amount to sponsor  
`From` - From address in case of allowance  
`Message` - Custom transfer message  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>