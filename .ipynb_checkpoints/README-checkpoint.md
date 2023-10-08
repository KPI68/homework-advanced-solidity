# homework-advanced-solidity

## Summary

This is a homework exploring ERC-20 compliant token deployment using Remix, MetaMask, and Ganache. We create a token named KaseiCoin (KAI), and deploy via crowdsale. This crowdsale features a goal, opening and closing time.

## Evaluation Evidence

With 3 contracts, one for the token, one for the crowdsale, one for the deployment, we deploy the "deployer" in Remix via Injected Provide - MetaMask. When this happens the other two contracts are created automatically.

### Deploy Deployer
![deploy_deployer](Images/deploy_deployer.png)

#### The contracts deployed
The token and its crowdsale

![deploy_contracts](Images/deploy_contracts.png)

#### The deploy transaction
The transaction shown at Ganache

![deploy_trans](Images/deploy_trans.png)

#### The crowdsale contract
Call up the crowdsale contract at Remix using its address

![crowdsale_contract](Images/crowdsale_contract.png)

#### The token contract
Call up the token contract at Remix using its address

![token](Images/token_contract.png)

### Buy tokens

#### Buy 10 ETH worthy from 335
Buy:

![buy_335](Images/buy_10_335.png)

Confirm at MetaMask:

![buy_335_confirm](Images/buy_10_335_metamask.png)

Bought:

![buy_335_confirm](Images/buy_10_335_balance.png)

#### Buy 15 ETH worthy from 9d3

![buy_9d3](Images/buy_15_9d3.png)

#### Buy 3 ETH worthy from 759

![buy_759](Images/buy_3_759.png)

### Total minted and fund raised

![minted](Images/total_supply.png)

![raised](Images/wei_raised.png)

### Finalize the crowdsale

When the closing time was 1 week, although the goal of 33 ETH worthy reached, the finalize call failed.

![finalize_fail](Images/finalize_fail.png)

Had to redeploy with the changed closing time as 5 minutes. Then, first tried to buy 35 ETH worthy, failed (exceeding cap).

![buy_fail](Images/buy_fail.png)

#### Before finalize

The wei raised not going to the proceeding wallet:

![before](Images/wallet_before_finalize.png)

#### finalize

Then bought exact goal 33 ETH worthy, and finalized.

![finalize](Images/finalize.png)

#### After finalize

The fund raised now got into the wallet.

![after](Images/wallet_after_finalize.png)
