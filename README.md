<p align="center">
  <img src="https://raw.githubusercontent.com/krakintgithub/solidity/master/cofounder_token/Logo_sm.png" width="150px" title="Logo">
</p>

## Krakin't Co-Founder token - BEP-20 standard - Technical Documentation
## Address: 0x4180CE5a616E75512fd9DF0bd896AC955C64a246

### About BEP-20 
Since this is not the main KRK token, we have issued the KRc (The Krakin't Co-founder token) on the Binance Smart-Chain, in order to save the GAS money.
Instead of Ethereum, BEP-20 works on the Binance token (BNB). You can use the Ethereum tools such as Metamask, however, you will have to add the Binance network.
<a href="https://docs.binance.org/smart-chain/wallet/metamask.html">Click here to learn how to adjust Metamask</a>

### Introduction 

The main purpose of this token is to develop a decentralized system that would aid the development of the Krakin't project. The amount of tokens someone holds will determine the strength of their vote.
The voting system will be done by applying the weighted inverse voting, where the amount of tokens will act only as a weight in the voting process.
Anyone who holds any amount of this token will be able to vote for the steps they believe Krakin't should take or avoid.

Furthermore, this token is based on an honour system, where anyone can claim tokens, as many times as they want!
We have borrowed the BTC model to controll the supply. Making a claim is equivalent to mining a block. Although we start with 50 tokens per claim and reduce the amount each epoch (210000 calls) by half, we also increase the amount of calls in the next epoch by 1/2 of the current epoch.

A Dapp for claiming the tokens is not necessary, while the process consists of the following steps:

- Setup the Metamask to work with the Binance chain (BSC)
- Deposit BNB to your 0x address
- Go to https://bscscan.com/address/0x4180ce5a616e75512fd9df0bd896ac955c64a246#writeContract
- Press Connect to Web3 (and accept everything for Metamask)
- Press the "Write" button under "4. Claim Tokens"
- Accept the transaction with Metamask

You may also claim to someone else's address using the "5. claimTokensTo" and providing their address

Please note:
- The token is initiated with 0 KRK, and claiming is equivalent to mining
- There are no pools, and pools are not necessary to have
- It is undecided how many tokens Krakin't will own. This will be determined by voting.
- There is only one claim per call
- Krakin't can mint and burn as many tokens as it is necessary to provide liquidity, do the presale, and anything else to establish the token environment
- Users will vote on chaning the ownership address to address(0) when the right time comes, and then, this token will have no owner (it will belong to a community).




### Source code analysis
This token has the basic token code taken from Open Zepellin. However, we have only added a few classes:

- claimTokens : for claiming the tokens to user's account
- claimTokensTo : for claiming the tokens to someone else's address
- mintTo : for mining tokens to some other address (for example, exchanges). This is Admin only.
- burnFrom : to burn tokens from address, in case there is an error or abuse. This is Admin only.
- changeOwner : to change the owner of a contract, or remove the existing one. This is Admin only.

