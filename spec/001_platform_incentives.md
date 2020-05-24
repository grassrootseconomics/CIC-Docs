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

## Currently
Grassroots Economics started with a pool of 8 Million Sarafu tokens (which they value 1:1 with Kenyan Shillings ala buy backs). Of which 90% will have been distributed to users as below by the end of April 2020. 
The following are all rules are platform based (not blockchain contract based). Note that these rules are for the Sarafu CIC only and are not meant to be the rules for other CIC creators.
### Disbursement Policies (Shown as Disbursement in database)
1. *airdrop-self-service*: New users get 50 Sarafu (a CIC) 
1. *airdrop-full-profile*: New users that fill out their profiles (name, business, location, gender) get additional 400 Sarafu (a CIC) (must call office line)
1. *referral bonus*: Users that are the 1st to send a new user at least 20 tokens in the 1st 24 hours get 100 Sarafu - after that new user has begun to trade with another user (not the referrer) 
1. *chama bonus*: Savings Groups (aka Chamas are groups of users that save and give loans to eachother) get 10,000 Sarafu divided between their members after 2 months of trading.
1. *usage bonus*: Users get a daily or weekly Sarafu bonues depending on how they trade. They are ranked by the number of other people they trade above 20 Sarafu with and awarded based on their percentage of such overall trade. (Possibly moving to k-cycle centrality).
1. *Donation bonus* Anyone with Mpesa or Bonga points can send them to Grassroots Economics to receive additional Sarafu. Donors can give Grassroots Economics funds to support the Sarafu buy-back and operations
### Redemption Policies (Shown as Agent_out in database)
1. *chama redemption*: Savings Groups can redeem 50% of their Sarafu Balance for Kenyan Shillings up to a maximum of 30k Sarafu each month but must have spent (and/or given loans) of at least as much as they want to cash out.  Cashing out is done using donor funds by Grassroots Economics Foundation and Sarafu is valued 1:1 with Kenyan shilligns using eMoney (Mpesa).
### Reclamation Policies (Shown as Reclaimation in database)
1. *Holding Fee*: If an account if dormant (no trades in or out) for 7 days 20 Sarafu are deducted and added back to the pool. 


## After
After the migration to xDAI (https://github.com/GrassrootsEconomics/CIC-Docs/blob/master/spec/xdai_migration.md) 
anyone (with access to blockchain) in the world can contribute reserve in the form of xDAI. xDAI is a stable token to the US dollar and can be purchased with USD. 
With a reserve in xDAI each Sarafu token will now have spot price or excahnge price to xDAI given by P = R/(SxTRR)
Where R = the amount of xDAI in reserve, S= the total supply of Sarafu, and TRR = Target Reserve Ratio = that ratio of R/S such that the echange price is 1:1.
1. Grassroots Economics will continue with all the above incentives for Sarafu and to buy the vouchers off on a regular basis 1:1 from Savings groups.

### Bonding Curve Economic Policies
1. *Targeted Reserve ratio*: Targeted reserve ratio of 25% collateral (4 Ksh of CICs issued for every 1 KSh in reserve)
1. *Transaction fees*: A % fee on conversion between reserve and supply in both directions is done on blockchain and added to the reserve.
1. *BondtoMint*: If the reserve of xDAI is depleted below accepted tolerance levels, Grassroots Economics (and other donors with webApp or Metamask) can add more xDAI reserve and mint more Sarafu tokens at cheaper exchange rates to spend or distribute according to disbursement policies. Any funds going into the reserve will increase the price and mint additional Sarafu following the bonding curve.
1. *BurntoWithdraw*: If the reserve of xDAI exceeds accepted tolerance levels, Grassroots Economics (and other donors with webApp or Metamask) can burn Sarafu and withdraw excess xDAI reserve at favorable exchange rates. Any funds removed from the reserve will decrease the price and burn existing Sarafu following the bonding curve. Grassroots Economics can destroy Sarafu it collects to pull out excess reserve and convert that xDAI to Kenyan shillings to continue with Savings Group buy backs according to redemption policies.

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
