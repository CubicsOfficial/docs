# Vote

## Explanation
Voting pools enable users to vote on a numeric outcome such as budgets and prediction markets, or on candidates, based on a predefined list of choices. Answer-based vote pools can resolve in multiple ways and reward the creator, the top candidate, the voters who voted correctly, or the voters of an answer that was set through an oracle. Rewarding voters of the most voted answer or the answer as set by an oracle, allows voting pools to be used as betting games with reward functionality.

To submit a vote, visit the vote pool page, connect your wallet and click on vote. You will be able to specify a number or answer that you would like to vote on, as well as an amount to add weight to your vote. If the voting mechanism is set to reward voters, voters can claim rewards after the voting pool resolves.

To create a vote, connect your wallet and click on “new pool” under wallet actions. You will be able to specify a list of candidates to create a choice-based vote, as well as the mechanism of resolution after the vote expires.

## Intro
The voting pool allows participants to vote on a numeric outcome (such as bets, estimations, budgets, prediction markets) or on an outcome based on provided answers. Voting pools can require a contribution amount, which serves as a weight for the vote. Vote pools can be resolved using various mechanisms: transferring all collected tokens to the creator, the highest candidate, or the voters (by the highest voted answer or through oracle result).

*Use Cases:  
Voting on a numeric outcome (bets, estimations, budgets, prediction markets)  
Voting on an answer outcome (guesses, candidates, tokens, proposals)  
Voting by collecting funds and rewarding the vote pool creator  
Voting by collecting funds and rewarding the highest voted candidate  
Voting by collecting funds and rewarding voters of the highest voted answer  
Voting by collecting funds and rewarding voters of the correct answer, as determined by an oracle*

## Functionality
A creator creates a voting pool and specifies the participation token, resolution mechanism, and optional candidates. Optionally, a minimum/maximum participation amount can be specified. Voters can then vote by providing a numerical answer (if the voting pool is a numerical vote) or by providing one of the specified answer candidates. Every vote can be weighted by the CUBIC participation amount. After the vote expires, it can be resolved based on the specified resolution mechanism. The mechanism rewards the creator, candidates or voters of the highest voted answer or the correct answer as determined by an oracle. If the mechanism rewards voters of the highest or correct answer, they can claim their rewards proportional to their weighted vote.

## Methods

### Transfer
Participate in the voting pool by providing a numerical answer or a candidate from the available choices.

**Requirements:** `None`  
**Outputs:** `Transfer claim from pool to sender`  
**Inputs:**  
`Amount` - CUBIC amount to add weight to the vote  
`Answer` - Choice from available candidates  
`Number` - Number if the vote is numerical  

### Claim
Allows claiming rewards, proportional to the weighted vote divided by the total weight of the winning vote.

**Requirements:** `Claim with valid answer`  
**Outputs:** `Reward transfer from pool to sender`  
**Inputs:**  
`Claim` - Claim hash  

### Resolve
Resolves vote using the specified vote-pool mechanism. Pays collected CUBIC weight amounts to either creator, top candidate or enables voters of the highest answer to claim their rewards.

**Requirements:** `Vote mechanism != oracle`  
**Outputs:** `Rewards transfer from pool to creator/candidate`  
**Inputs:** `None`  

### Create
Creates a voting pool, with a numerical or candidate type and a specific resolution mechanism.

**Requirements:** `None`  
**Outputs:** `Vote pool`  
**Inputs:**  
`Mechanism` - Resolution mechanism, creator, candidate, voters, oracle  
`Candidates`- List of candidates to vote on, numerical vote if empty  
`MinAmount` - Minimum amount to participate in vote  
`MaxAmount` - Maximum amount to participate in vote  
`TransfersLimit` - Maximum number of votes  
`ClaimsLimit` - Maximum number of winning votes for top candidate  
`CubicsLimit` - Maximum collected CUBIC as vote-weights  
`Expires` - Datetime when the vote expires  

### Oracle
The creator can set the correct answer so voters who claimed that answer can claim their rewards.

**Requirements:** `Pool creator`, `Candidate pool`, `Pool mechanism = oracle`  
**Outputs:** `None`  
**Inputs:**  
`Answer` - Correct answer  

<div style="page-break-after: always; visibility: hidden">\pagebreak</div>