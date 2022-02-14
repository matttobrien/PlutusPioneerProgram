## Overview
The homework for this week was to implement several functions in Homework1.hs and Homework2.hs. The lesson this week focused on Native Assets on Cardano; How to mint and burn fundgitable & non-fungible tokens (NFTs) using plutus smart contracts.
 
## Homework1
The goal of homeword 1 was to create a native asset policy which should only allow minting (or burning) of tokens if the owner of the specified PaymentPubKeyHash has signed the transaction and if the specified deadline has not passed. The first case can be validated using the txSignedBy function, passing in the context and public key hash parameter. Then the second case can be validated using to and contains to check if the range provided in the transaction context is before the specified deadline.
 
## Homework2
The goal of homework 2 was to create a minting policy for an NFT, where the minting transaction must consume the given UTxO as input and where the TokenName will be an empty ByteString. This can be achieved by first checking if the transaction contains any UTxOs (hasUTxO helper function), then checking if the provided (or should I say unprovided) token name is an empty bytestring, and ensuring the amount requested to be minted is 1 (checkMintedAmount helper function). These checks ensure the NFT created is truly one of a kind, as a unique UTxO is used to forge the NFT.
