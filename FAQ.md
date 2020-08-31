# Frequently Asked Questions

## What is StealthSwap?

StealthSwap is an Ethereum smart contract based protocol that allows one party to send funds to another using stealth addresses. 
That address is controlled by the recipient, but that information is obfuscated and only limited to the participants.

## Does StealthSwap hold any funds

NO, the contracts are oracle that publish events and authenticate and verify user's transactions.
No funds are held by the contracts.

## What does StealthSwap do different than other anonymity protocols

Other anonymity protocols on Ethereum include [Tornado Cash](https://tornado.cash/)
a zkSNARKs based on chain mixer. Unlike other mixing protocols it uses zero-knowledge
proofs to verify your withdrawal address breaking the link between the origin and withdrawal address.

StealthSwap is meant for direct payments between two parties, and has different privacy tradeoffs.
Instead of breaking the link between the sender and recipient StealthSwap makes it meaningless.
Another trade-off is gas, zkSNARKs require higher gas and thus higher fees, StealthSwap optimizes
gas fees up to 89%.
One more trade-off is usage on-chain mixers are limited to pooling and withdrawals, while
StealthSwap could be used by any dApp in the ecosystem, it's essentially a privacy protocol not just
an app.

## What are the advantages of StealthSwap

* StealthSwap allows any amounts to be sent, unlike mixers it doesn't require uniform amounts.
* StealthSwap has no  time bounds for withdrawing funds— once they are sent the funds can be withdrawn to any address the receiver chooses.
* StealthSwap ensures only the receiver can withdraw the funds once they're sent.
* StealthSwap uses significantly less gas, as it does not require the verification of any advanced zkSNARK circuits on chains. All transactions are simple transfers.
* StealthSwap enables ETH and arbitrary ERC20 tokens to be transferred privately. You're not dependent on a large anonymity set developing for each token.

## Uses cases

### DEX Trades

Alice owns *x* ETH and wants to receive *y* OWLs, Alice can use her StealthSwap address to receive tokens, effectively eliminating
all links between her exchanged ether and received tokens.

### Payments

Alice has a new project in mind and hires Bob to do some work for her. She and Bob agree to a weekly rate.

Upon his visit to the StealthSwap Pay app, he sets up his account, enabling hime to be paid privately. Alice uses StealthSwap to sendBob his commission and she only requires his ENS address.

On chain, we see Alice pays a different and empty address each week. Bob controls the keys to each of these addresses via StealthSwap, but this information is unknown to anyone except Alice and Bob.

Bob uses StealthSwap to withdraw his funds to any address, because StealthSwap uses Gas Station Network and Uniswap, Bob doesn't have to fund the stealth address with Ether to withdraw his funds. He can pay for gas with the funds he received. 
