# TransactionDatasets
Data Sets from Blockchain Transactions and User Demographics

Datasets prior to 2020 are pulled from the POA blockchain for each user ex. https://blockscout.com/poa/core/address/0xcb55fc893000a984a5ad73011f93d1540a5f0895/tokens
As well as user generated data and field surveys collected in Kenya. Fields described below.

Datasets Starting 2020 are pulled from the POA (xDAI) blockchain for each user ex. https://blockscout.com/poa/core/address/0xcb55fc893000a984a5ad73011f93d1540a5f0895/tokens
As well as user generated data and field surveys collected in Kenya. Fields described below.

Brief description: Using a simple feature phone interface with USSD each user (people living below the poverty line in Kenya) starts with 400 Tokens and adverstises what they sell on a digital market place avalaible on the same interface. There are no transaction fees. The tokens are used often as a top-up to missing Kenyan shillings. Certian users / vendors were allowed to send 50% of their tokens to Grassroots Economics (GE) in return for Kenyan Shillings on a monthly basis. Each user only has one token assigned to them by GE based on where they live (Currently we have moved all users to the Sarafu token while we prepare for the next phase). When a user sends a token to another user that holds a different token a conversion is made automatically after receipt. This conversion uses a bonding curve (based on the Bancor Protocol) to adjust the token prices relative to eachother. Conversions can be seen as transactions to a contract address then that contract address sending the new token to the user. While the exchange rate information is avaliable to users, practially all the tokens are curently considered ~1:1 with the national currency as well as with eachother. For more information please contact us https://www.grassrootseconomics.org/contact


--------

Post 2020 xDAI
The Transaction csv fields:

1. id - internal transaction ID number
1. timeset - date and time of transaction
1. transfer_subtype - internal typing: DISBURSMENT = from Grassroots Economics, RECLEMATION = Back to GE, STANDARD =  a trade between users, AGENT = when a group account is cashing out (see held_roles) below
1. transfer_use - The category the sender marked the transaction as - used for 'confidence' later for the user category - note this will be changed to boolean
1. tx_hash - hashed transaction address on blockchain 
1. source - wallet ID of sender 
1. s_comm_tkn - Short name of Token that the source uses (each user should only have 1 token) - note that currently all users have Sarafu only
1. s_gender - From user input
1. s_location - Village name, From user input
1. s_business_type - Entered by GE staff based on user inputed products or services
1. target - wallet ID of recipent 
1. t_comm_tkn
1. t_gender
1. t_location
1. t_business_type
1. token_name - the token that was traded
1. token_address - the blockchain address of token that was traded
1. weight - How many tokens were traded

The user summary csv fields:

1. id - Internal user id number
1. xDAI_blockchain_address - Wallet ID on POA xDAI Blockchain 
1. old_POA__blockchain_address - Wallet ID on POA Blockchain if they had one
1. comm_tkn - Their token name (each user only has 1 token) currenlty only Sarafu
1. bal - current balance of [comm_tkn] as of file date
1. location - User input (village name) 
1. held_roles - Standard transactions are between Beneficiaries, anything to an Admin is a Reclemation or from and Admin is a Disbursment and anything to a Agent is a Agent_out
1. gender
1. business_type - Input by GE staff based on what the users sell
1. ovol_in - total number of tokens that came into this account from non-STANDARD transactions
1. ovol_out
1. otxns_in - number of transactions incomming from non-STANDARD transactions
1. otxns_out
1. ounique_in - number of uniquie transactions incomming from non-STANDARD transactions
1. ounique_in
1. svol_in - total number of tokens that came into this account from STANDARD transactions
1. svol_out
1. stxns_in - number of transactions incomming from STANDARD transactions
1. stxns_out
1. sunique_in - number of uniquie transactions incomming from STANDARD transactions
1. sunique_in
1. start - day and time of first transaction (when the user account was setup)
1. confidence - based on how many other purchasing users agree with the business_type

----

Pre 2020 POA
The Transaction csv fields:
1. timeset - date and time of transaction
1. tx_hash - hashed transaction on blockchain can be found on https://blockscout.com/poa/core/a
1. source - wallet ID of sender can be found on https://blockscout.com/poa/core/a - which could be a contract (for a conversion)
1. s_comm_tkn - Short name of Token that the source uses (each user should only have 1 token)
1. s_gender - From user input
1. s_location - From user input
1. s_business_type - Grassroots Economics Staff
1. s_directory - From user input
1. target - wallet ID of recipent - which could be a contract (for a conversion)
1. t_comm_tkn
1. t_gender
1. t_location
1. t_business_type
1. t_directory
1. tx_token - the token that was traded
1. weight - How many tokens were traded
1. id - test variable


The user summary csv fields:
1. id - Wallet ID on POA Blockchain - can be found on https://blockscout.com/poa/core/a
1. comm_tkn - Their token name (each user only has 1 token)
1. bal - current balance of [comm_tkn] as of file date
1. location - User input (village name)
1. gender
1. business_type - Input by staff based on what they sell
1. directory - input by user a specific item they sell
1. vol_trans_in - total number of tokens that came into this account
1. vol_trans_out
1. n_trans_in - number of transactions incomming
1. n_trans_out
1. n_in_unique - number of uniquie transactions incomming
1. n_out_unique
1. start - day and time of first transaction (when the user account was setup)
