# CobinhoodBuyer

Changes from original MonethaBuyer contract:
* removed all bounties (no need, this is a closed group and it's presale, so don't need to rush. And it's too late for bug bounty).
* changed constants, such as caps, timestamp window, developer address, presale contract address, etc.
* removed the ability for developer to set contract address (hard coded it instead)
* because the Cobinhood contract doesn't return tokens right away, needed to change the `bought_tokens` flag to `purchased_tokens` and `received_tokens`, and updated the related logic

## Procedure
1.  I will send the CobinhoodBuyer contract to the blockchain and then share the address of it
2.  Everyone will send their ETH to the address of the CobinhoodBuyer contract
3.  Once everyone sends their ETH to the CobinhoodBuyer contract, I will call the purchase() function to send all the ETH to the Cobinhood presale contract
4.  We wait for Cobinhood to release tokens at some later date.
5.  We all individually call withdraw() on our own addresses to receive our share of the tokens. (I can write a helper function for this if necessary.)
