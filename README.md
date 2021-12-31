## Uses:

1. Leveraged Arbitrage
2. Swapping collateral out of loaned positions, without having to repay the debt of the loaned position

Flash loan - borrow the money and repay it back in the exact same transaction. Lender takes a small fees for providing this i.e. premium and a little bit of gas fees

### Aave Flash Loan Brownie Mix - https://github.com/PatrickAlphaC/aave-flashloan-mix

This Brownie mix comes with everything you need to start developing on flash loans.

This mix is configured for use with Ganache on a forked mainnet.

If you're unfamiliar with environment variables you can just add all these commands to your .env file and run source .env when you're done.

If using metamask, you'll have to add a 0x to the start of your private key

Aave is the go to platform for borrowing and lending

We will deploy this on Kovan testnet and hence don't need Ganache CLI, but If you do want to test locally then go ahead with that setup.

Main code => FlashloanV2.sol under contracts folder

Here we will write a flash loan for some WETH. After adding all credentials in your .env file simply run this from terminal source .env

We will require some WETH to pay the premium / fee of the flash loan

In the get_weth.py we will deposit one testnet ETH to get one KETH or testnet Ether for Kovan

Wrapped ETH, or WETH, is a token that represents ETH 1:1 and conforms to the ERC20 token standard. By conforming to ERC20, it allows for increased functionality across any application that handles ERC20 tokens. You can always convert your WETH to ETH 1:1 and vice versa.

<img width="604" alt="Screenshot 2021-12-31 at 6 39 11 PM" src="https://user-images.githubusercontent.com/57283161/147825064-e013f9f9-626a-4cb0-a544-b0839c903837.png">

## Deploying our flashoan contract

Through this flashloan we simply borrowed 1 WETH, got AAVE interest bearing token in return and then gave back that 1 WETH + some fees to AAVE

<img width="620" alt="Screenshot 2021-12-31 at 6 39 49 PM" src="https://user-images.githubusercontent.com/57283161/147825079-b750d62c-fb4c-4c25-9291-37e7e7811fd1.png">

<img width="624" alt="Screenshot 2021-12-31 at 6 40 17 PM" src="https://user-images.githubusercontent.com/57283161/147825103-8fbb486c-4814-40ec-b023-d888f64883a2.png">
<img width="625" alt="Screenshot 2021-12-31 at 6 40 29 PM" src="https://user-images.githubusercontent.com/57283161/147825110-64cc581c-a3cd-47db-8021-dd07f23bac5b.png">
