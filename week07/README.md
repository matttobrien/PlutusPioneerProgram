## Overview
The homework for this week was to implement the game Rock Paper Scissors as a Smart Contract, using the provided StateMachine.hs as a guide.

The orginal StateMachine.hs game involves two users, where each user can select either a '0' or a '1' and bet a number of lovelace that thier number will beat the other. The rules are as follows:

            Bob 
            0  1
        __|__ __ 
Alice  0  | A  B
       1  | B  A
      
This diagram represents that if Alice goes first, and they both select the same number, Alice wins. If Alice goes first and Bob selects a different number, then Bob wins. Sounds pretty simple right. However, the issue with playing this game over text, email, etc. Is that Alice would be sending her selection first, Bob will see it, and then make his decision. If Bob can not be trusted to play fair, then this is not a fair game. 

A simple cryptographic way around this is to hash Alice's choice, and append it with a nonce, to ensure the hash will always be different. Therefore, Bob cannot guess Alice's choice based on what he recieves. After Bob sends his choice back (it can be in plain text), Alice can determine the outcome of the game, and send her choice along with the nonce to Bob, so that he can verify the result.

## Homework
The goal was to create a Rock Paper Scissors game, using the provided StateMachine.hs as a basis. In order to do this, the GameChoice had to be modified to have our new three choices, while also accounting for a draw. A new transition case also had to be added to the State Machine to hand the case of a draw.