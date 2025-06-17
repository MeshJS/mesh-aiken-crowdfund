# Aiken Gov Crowdfunding

## 1. Spend

The spending validator that guarding the crowdfunded

## 2. Stake

The token that represents lovelace contributed to current crowdfunding campaign

## 3. Start

The withdrawal script that oversight the completion of crowdfunding (i.e. `completion_script` at crowdfunding script)

## Param dependency tree

1. First layer

   - `auth_token` - no param

2. Second layer

   - `shares` - param `auth_token`
   - `crowdfund` - param `auth_token`
