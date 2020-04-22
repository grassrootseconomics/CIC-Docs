# Title

<!--
valid status values are: Pre-draft
-->
* Authors: Will Ruddick <will@grassecon.org>
* Date: 2020.04.22
* Version: 1
* Status: Pre-draft

## Rationale
We want to give donors and community mambers a way to contribute to and cash out from Community Inclusion Currencies with National Currency. By connecting to a reserve that is stable to the US dollar called xDAI we bring some stability and the ability for many to support local communities. We also enable any CICs that have xDAI as a reserve to convert to any other CIC with xDAI as reserve. 

## Before 
Currently we are using a virtual reserve a generic ERC20 token. We have 2 Million of those reserve tokens against 8 Million Sarafu issued (the current Kenyan CIC). Sall those Sarafu_1 or S1

## After
We have 40,000 xDAI to put as the reserve and are looking at minting 16Million tokens called Sarafu  S2
with a connector weight (target Reserve Ratio) of 0.25 (25%) and an inital price of roughly 0.01 Sarafu to a xDAI (USD stable)

## Implementation
Each existing user should have a completley new wallet and private key for security reasons and be given the same balances they currently have with the new (xDAI reserve) Sarafu.

### Workflow
1. Synch db <->Blockchain
1. Deply contracts to create Sarafu_2 - deposit reserve and mint tokens
1. Migration - New wallets for users - Replicate user accounts with new token Sarafu_2

### Variables

1. Synch variables, - synch frequency - and limitations
2. Contract variables (reserve ratio, reserve amount, number of Sarafu_2)
3. Migration speed 

### Interface
This will all be done at code and command line level

## Testing
1. Check db<->blockchain synch - verify they are synched and we can do external transactions and handle RPC failure
1. Contract deplyment - conversions, transfers all work as expected 
1. Migration - new wallets match old wallets
1. Store old blockchain wallet IDs (as a list with old POA wallets)


## Changelog
<!--
Please remember to describe every change to this document in the changelog using 
serial number:

* version 1:
-->
