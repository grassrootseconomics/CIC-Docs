# Current Platform Incentives spec

<!--
valid status values are: Pre-draft|Draft|Proposal|Accepted
-->
* Authors: Will Ruddick <willruddick@gmail.com> (grassecon.org)
* Date: 2020.04.22
* Version: 1
* Status: Pre-draft

## Rationale
The current system seeks to maximize circulation in order to fill market gaps and help CIC users to support eachother.

## Before 
Currently:
1. Grassroots Economics started with a pool of 8 Million Sarafu tokens (which they value 1:1 with Kenyan Shillings ala buy backs). Of which 90% will have been distributed to users as below by the end of April 2020.
1. New users get 400 Sarafu (a CIC)
1. Users that refer other users get 100 Sarafu - after that new user has begun to trade
1. Savings Groups (aka Chamas are groups of users that save and give loans to eachother) get 10,000 Sarafu divided between their members after 2 months of trading.
1. Savings Groups can redeem 40% of their Sarafu Balance for Kenyan Shillings each month but must have spent (given loans) of at least as much as they want to cash out. 
1. Cashing out is done using donor funds by Grassroots Economics Foundation and Sarafu is valued 1:1 with Kenyan shilligns using eMoney (Mpesa).
1. Users get a daily or weekly Sarafu bonues depending on how they trade. They are ranked by degree of uniquie outward trade above 20 Sarafu centrality and awarded based on their percentage of overall centrality. (Possibly moving to k-cycle centrality).
1. Holding Fee: If an account if dormant (no trades in or out) for 7 days 20 Sarafu are deducted and added back to the pool
1. Anyone with Mpesa or Bonga points can send them to Grassroots Eocnomics to receive additional Sarafu
1. Donors can give Grassroots Economics funds to support the Sarafu buy-back and operations

## After
After the migration to xDAI (https://github.com/GrassrootsEconomics/CIC-Docs/blob/master/spec/xdai_migration.md) 
anyone (with access to blockchain) in the world can contribute reserve in the form of xDAI. xDAI is a stable token to the US dollar and can be purchased with USD. 
With a reserve in xDAI each Sarafu token will now have spot price or excahnge price to xDAI given by P = R/(S*TRR)
Where R = the amount of xDAI in reserve, S= the total supply of Sarafu, and TRR = Target Reserve Ratio = that ratio of R/S such that the echange price is 1:1.
1. Grassroots Economics will continue to buy the vouchers off on a regular basis 1:1 from Savings groups.
1. Any funds going into the reserve will increase the price and mint additional Sarafu following a bonding curve.
1. Grassroots Economics will destroy Sarafu to pull out excess reserve and convert that xDAI to Kenyan shillings to continue.
1. Anyone with a webApp or MetaMask can add xDAI and mint more Sarafu (+) increase the value of all Sarafu
1. Anyone with a webApp or MetaMask can add send Sarafu to the converter contract to destry it and withdraw reserve (-) decreasing the value of all Sarafu


## Implementation

### Workflow

### Variables

### Interface


## Testing
<!--
Please describe what test vectors that are required for this implementation
-->

## Changelog
<!--
Please remember to describe every change to this document in the changelog using 
serial number:

* version 1:
-->
