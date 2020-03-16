# Depth Bump - Add new tokens to reserve and supply with a specified price

Author: Will Ruddick
Version: 0.0.1

## Rationale

Moving to xDAI looks unstable right now. In order to increase our token supply we can increase the amount of virtual reserve and CIC supply and keep the price fixed.

## Before

We have a virtual token right now as the reserve.

## After

We would need to be able to mint tokens and the reserve outside of the bonding curve.
The idea would be to keep the price 1:1 with reserve and increase both reserve and supply (off the curve)

## Implementation

* return ownership of the token to a person (not the converter)
* mint more tokens (off the curve)'
* give ownership back to the converter
* add more virtual reserve to the converter

## Variables

* Amount of supply to add S2 16,000,000
* Amount of Reserve to add R2 8,000,000
* Resulting Exchange Price: P2 1.0

* Existing CIC Supply: S1 ~8,000,000
* Existing Reserve: R1 ~2,000,000
* Existing Price: P1 ~1.0

## Testing


cmd: depthbump targetsupply=16000000.0 price=1.0
You are creating (16000000.0 - S1) new tokens? (yes/no/quit)
You are creating ((16000000.0)/4-R1)*P2 new reserve tokens? (yes/no/quit)

....
the new supply of CIC should be: 16,000,000
the new reserve should be: 4,000,000

(error if P2 != 4(R1+R2)/(S1+S2)) (where 4 is 1/cw from converter contract)
(warning if P2 != P1 and confirmation)


## Changelog

* 0.1: Created initial stub
