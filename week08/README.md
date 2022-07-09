## Overview
The homework for this week was to modify the token sale contract so that it accepts an additional transition called "close" that can be called only by the seller to close the UTXO, and collect all the remaining tokens, lovelace and the NFT.

## Homework
The goal was to modify TokenSale and TSRedeemer to accept an new close transaction. The changes required were to the modify the Datum type State to Maybe Integer, and create the case "close" to close the token sale. The type signatures for the state machine, validator, and ts client were also updated accordingly.