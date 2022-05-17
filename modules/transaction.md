# Transaction

## Explanation
Cubics transactions are blocks of instructions that are executed by Cubics validator nodes. Instructions can specify multiple functions and enable batch actions such as minting multiple tokens or sending multiple transfers in one transaction. Transactions have a fee associated with them, based on the number of functions calls, reads, and writes, that each instruction executes.

After a transaction is submitted, it is broadcasted to all validator nodes that process the transaction and return the computed result to the coordinator node. After consensus has been established, a transaction is considered confirmed and is stored permanently on the Cubics blockchain. Cubics transactions have an approximate one-second finality time with an average cost below a tenth of a cent.

Transactions are automatically created for any action you might perform on the Cubics network app. If you send a transfer, for example, it is automatically wrapped and submitted as a transaction by the Cubics client.