# Auth Token

## Parameter

## User Action

1. Instantiate Crowdfunding Campaign - Redeemer `RMint`

   - The only token (current policy) minted in this transaction is sent to `Crowdfund` address, with datum:

     - `completion_script` - matching the one in param
     - `share_token`: The policy ID of the share token
     - `crowdfund_address`: The address of the crowdfunding campaign
     - `fundraise_target` - The target fundraising amount
     - `current_fundraised_amount` - Storing the current fundraising amount
     - `allow_over_subscription`: Whether
     - `deadline` - The timstamp of the deadline
     - `expiry_buffer` - The buffer time of after deadline, for crowdfund initiator to execute `completion_script`
     - `fee_address`: The address that collect min utxo / additional fee at the end
     - `min_charge`: The minimal lovelace to be collected at completion of crowdfunding

   - The only token minted with token name `completion_script`
   - Min charge must be either 0 or min utxo (let's say 1 ada)

2. Burn - Redeemer `RBurn`

   - The current policy id only has negative minting value in transaction body.
