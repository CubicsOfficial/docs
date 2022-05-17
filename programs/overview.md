# Cubics Program Overview

Cubics focuses on gaming and metaverse applications that commonly require features such as auctions, voting, swapping. With Cubics, we provide 10 in-built programs, which can be specified as program when creating a new pool:

### [Auction](auction.md)
Auctions allow anyone to offer fungible or non-fungible tokens for sale. Bids are handled by the program, and auctions are considered successful when the auction pool has no target, the target is met, or the limit is met (equivalent to an instant purchase at maximum price).

### [Launch](launch.md)
Fundraising pools allow creators to raise CUBIC until a specific target or limit is met. Successful funds distribute portions of the raised amount to the creator and the remainder to the assets' swap pool as liquidity. If a pool rate is set, the fund automatically swaps CUBIC to asset tokens at that specified rate directly, without the condition of having to meet a fundraising goal.

### [Lending](lending.md)
Lending pools allow users to borrow tokens against CUBIC collateral. Lending pools allow “short selling” a token or resolving claims without owning the token. At the same time, it enables lenders to earn interest by making their tokens available for borrowers.

### [Lock](lock.md)
Locking pools allow asset owners to lock funds for various use-cases, such as delayed payouts and vesting.

### [Loot](loot.md)
Loot pools allow NFT creators and games to distribute (drop) new NFTs, items, skins from a collection in a randomized and engaging way. Users can enter for free or for a fee as specified by the pool creator. Entrants receive tickets that have a certain probability of winning a random item from the loot pool.

### [Lottery](lottery.md)
Promo pools provide an airdrop/lottery mechanism, which can engage users or distribute tokens in a simple and fair way. Users can participate for free or for a fee (specified upon pool creation) and receive tickets with a certain probability to win from the prize pool.

### [Royalty](royalty.md)
Royalty pools are set up by an asset creator who wishes to reward all or parts of his assets based on a specified daily rate. Currently, this finds application in providing NFTs with yield for holding (royalties).

### [Staking](staking.md)
Staking pools allow token creators to reward holders of fungible tokens, depending on lock-up length and amount. For example, a pool creator might specify a certain APY and bonus rate for his pool, deposit reward tokens, and allow users to lock up tokens into the pool who will receive rewards once their lock-up period expires.

### [Swap](swap.md)
Swapping pools are pools holding CUBIC and the pool asset, which can be exchanged one for another. Swap pools are the same functionality that makes popular DEXs like Uniswap or PancakeSwap possible.

### [Vote](vote.md)
Voting pools allow users to submit votes given a list of assets/addresses or numbers (prediction markets). Voting can be used for governance (voting for new proposals), for predictions with payouts to the winning voters, or to engage users (a mechanism to vote on any tokenized objects and get paid if the vote was correct after pool expiry).



# Programs

Cubics focuses on Gaming and Metaverse applications that frequently require features such as auctions, voting, swapping, and similar. Cubics provides ten in-built programs available as the underlying mechanism when creating a new asset pool. Asset pools are smart contracts that send and receive transactions while executing a set of pre-written instructions tied to an underlying asset.



* Auction
    * Auctions allow anyone to offer fungible or non-fungible tokens for sale. Bids are handled by the program, and auctions are considered successful when the auction pool has no target, the target is met, or the limit is met (equivalent to an instant purchase at maximum price).
* Launch
    * Fundraising pools allow creators to raise CUBIC until a specific target or limit is met. Successful funds distribute portions of the raised amount to the creator and the remainder to the assets' swap pool as liquidity. If a pool rate is set, the fund automatically swaps CUBIC to asset tokens at that specified rate directly, without the condition of having to meet a fundraising goal.
* Lending
    * Lending pools allow users to borrow tokens against CUBIC collateral. Lending pools allow “short selling” a token or resolving claims without owning the token. At the same time, it enables lenders to earn interest by making their tokens available for borrowers.
* Lock
    * Locking pools allow asset owners to lock funds for various use-cases, such as delayed payouts and vesting.
* Loot
    * Loot pools allow NFT creators and games to distribute (drop) new NFTs, items, skins from a collection in a randomized and engaging way. Users can enter for free or for a fee as specified by the pool creator. Entrants receive tickets that have a certain probability of winning a random item from the loot pool.
* Lottery
    * Promo pools provide an airdrop/lottery mechanism, which can engage users or distribute tokens in a simple and fair way. Users can participate for free or for a fee (specified upon pool creation) and receive tickets with a certain probability to win from the prize pool.
* Royalty
    * Royalty pools are set up by an asset creator who wishes to reward all or parts of his assets based on a specified daily rate. Currently, this finds application in providing NFTs with yield for holding (royalties).
* Staking
    * Staking pools allow token creators to reward holders of fungible tokens, depending on lock-up length and amount. For example, a pool creator might specify a certain APY and bonus rate for his pool, deposit reward tokens, and allow users to lock up tokens into the pool who will receive rewards once their lock-up period expires.
* Swap
    * Swapping pools are pools holding CUBIC and the pool asset, which can be exchanged one for another. Swap pools are the same functionality that makes popular DEXs like Uniswap or PancakeSwap possible.
* Vote
    * Voting pools allow users to submit votes given a list of assets/addresses or numbers (prediction markets). Voting can be used for governance (voting for new proposals), for predictions with payouts to the winning voters, or to engage users (a mechanism to vote on any tokenized objects and get paid if the vote was correct after pool expiry).




# Cubics Program Overview

## Explanation
Let me walk you through all official pool programs on Cubics. To start, let’s see why and when you might want to use a pool. Pools enable trustless execution of code through prewritten programs. When you deal with another party, trust plays an essential part in the transaction. With pools, you can simply trust that the program will execute the code instead of relying on human integrity.

There are ten prewritten programs on Cubics, which have been extensively tested and verified. Let’s look at each pool program and explain what they are used for.

Auction programs enable creators to sell their NFT. Users submit bids to the auction pool, and upon completion, the pool automatically transfers the assets to the individual parties depending on the success of the auction.

Launch programs enable projects to raise funds by distributing tokens to participants who wish to contribute CUBIC tokens. The CUBIC contribution is added to the liquidity of the launched token and can be traded afterward through its swap pool. Participants in the launch can claim their share of tokens after the launch completes.

Lending programs enable the lending and borrowing of fungible tokens. Lenders can deposit tokens to earn interest, and borrowers can borrow tokens in exchange for CUBIC collateral.

Lock programs enable users to lock tokens for themselves, or for someone else. This might come in handy when a project wants to distribute tokens without making them available instantly.

Loot programs are dropzones, where NFT creators can launch and distribute their NFTs in a randomized way. Creators specify a win probability, and users can transfer the required participation amount to the loot pool. Every transfer has a chance to win a random NFT, dependent on the loot pool probability.

Lottery programs enable creators to run promotions for a prize, which can be a fungible token or an NFT. Users enter a lottery for free or for the minimum required contribution amount and receive a participation ticket otherwise known as a claim. Once the lottery completes, users can redeem their claim to see if they hold a winning ticket and receive their part of the prize.

Royalty pools allow users to earn passive income by holding NFTs. Creators of NFTs can set up a royalty pool and deposit reward tokens to it. Royalties accumulate day by day and can be claimed by holders of eligible NFTs, which are specified by the creator.

Staking programs enable token creators to offer rewards for locking tokens for a certain amount of time. Users can stake tokens, and receive interest as well as bonus tokens in return once their staking period expires.

Swap programs are simply decentralized exchanges operating through a mathematical swap function. After liquidity is added to a swap pool, users can swap CUBIC into tokens or vice versa in a fully trustless and open way.

Vote programs enable voting on numeric targets like budgets, prediction markets, or a predefined set of candidates. Furthermore, vote programs can create betting games that reward voters with the correct answer.

To create a pool, visit the Cubics network app and connect your wallet. Click on your wallet, and select “new pool” under your wallet actions. Specify the associated pool token as well as the program. Check the Cubics documentation for your selected program or the program explanation video to find out more about the program and any additional fields that you can use to customize your pool.