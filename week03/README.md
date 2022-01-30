## Overview
The homework for this week was again to fill in in the blanks in the Homework1.hs & Homework2.hs files provided in plutus-pioneer-program/code/week03/src/Week03. This week we did some more work with on-chain validator code.

The smart contract featured this week (Vesting.hs) allows a user to depost Ada into the script, set a beneficiary for the Ada and a deadline for when the funds can be withdrawn. It essentially locks up the coins until the deadline is reached and the beneficiary wallet interacts with the contract.

## Homework1
The goal of homework 1 was to implement the logic so that the script should validate if either beneficiary1 has signed the transaction and the current slot is before or at the deadline, or if beneficiary2 has signed the transaction and the deadline has passed. This can be easily implemented by making use of Haskells guards for pattern matching.

## Homework2
The goal of homework 2 was to work with the parameterized version of a contact where you can have an additinal input along with the datum, redeemer and context. For this task, the beneficiary wallet was to be provided through the parameter and the deadline through the datum. This required a few changes to the mkValidator, Vesting and typedValidator functions.
