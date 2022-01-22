# PlutusPioneerProgram

My homework done for the Plutus Pioneer Program Cohort 3. It is a program to recruit and train developers in Plutus for the Cardano ecosystem with the goal of learning the core principles of how to code in both Haskell and Plutus.

## To set up the environment
I followed this guide by renzwo: https://github.com/renzwo/cardano-plutus-apps-install-m1
This guide is for M1 macs, but it worked for me with one small change in step 4:
```bash
build-users-group = nixbld

substituters        = https://hydra.iohk.io https://iohk.cachix.org https://cache.nixos.org/
trusted-public-keys = hydra.iohk.io:f/Ea+s+dFdN+3Y/G+FDgSq+a5NEWhJGzdjvKNGv0/EQ= iohk.cachix.org-1:DpRUyj7h7V830dp/i6Nti+NEO2/nhblbov/8MW7Rqoo= cache.nixos.org-1:6NCHdD59X431o0gWypbMrAURkbJ16ZPMQFGspcDShjY=

sandbox = false
extra-sandbox-paths = /System/Library/Frameworks /System/Library/PrivateFrameworks /usr/lib /private/tmp /private/var/tmp /usr/bin/env
experimental-features = nix-command
extra-experimental-features = flakes
```
I removed the system section as my MACHTYPE was not x86_64-darwin. You can check your using % set | grep "MACHTYPE" in the terminal.

## To compile code
If you would like to compile the code in cabal repl:

1. clone the plutus pioneer program from the IOG repo:
```bash 
git clone https://github.com/input-output-hk/plutus-pioneer-program
```
2. start nix-shell
```bash 
nix-shell
```
3. nagvate to the section you would like to complile, for example:
```bash 
cd /plutus-pioneer-program/code/week02
```
4. run cabal build
```bash 
cabal build
```
5. another option is to use cabal repl to interact with the code
```bash 
cabal repl
```
6. Done!