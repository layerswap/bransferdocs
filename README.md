# Bransfer Docs Home

Welcome 👋 to the offical docs for Bransfer, the software that helps you save (money and time) on exchange to exchange crypto transfers.

## What? How?

You create withdrawal from one exchange. Exchange takes your withdrawal, validates bunch of stuff, uses bunch of cryptography to compose valid blockchain transaction and pushes it to blockchain network. Miners pick up your transaction. Ofcourse, if exchange was wise enough and put enough fees to compete with others. They start mining and mining, then after they finally find those `00000...` in the block hash they publish the block with your transaction. But that is not enough yet, you still have to wait for couple of more blocks to get minied, so your transaction can be called confirmed. 

![Standard withdrawal](/assets/standard_withdrawal.png)

The question we ask is, this is what we really wanted? Ok, this is cool stuff, cryptography, decentrailization and everything. But I am in centralized exchange and I want my crypto to be in another centralized exchange. Why I would go throught all these stuff, pay insanse amount of fees and wait not less insane amount of time?

Most of exchanges has internal transactions. When you create withdrawal from one exchange account to another one in same exchange. This is done almost instantly and with 0 fees as these transactions doesn't go throught blockchain. ([example Binance](https://www.binance.com/en/support/articles/360037037312-How-to-Make-Internal-Transfer-within-Binance)). 

![Bransfer withdrawal](/assets/bransfer_withdrawal.png)

Let's take in example binance and huboi. We create institutional accounts in both of them. Whenever you want to do withdraw from binance to huobi, you do withdrawal from your binance account to our binance account. We detect this transaction and create withdrawal from our huobi account to your huobi account. As you see both transactions are internal. You don't pay network fees (just throw coin to your witcher) and you almost don't wait, those are nearly instant.

We ❤️ crypto as much as you do (except one nerd). So don't immediatly start blaming us. We understand that this is not an crypto-way. We understand that we are centralized institutaion which is against decentralizaiton. We are horrible. Ok. But the issue still remains, there are centralized exchanges and we for no necassarity pay a lot of time and money for e2e transactions.

You are probably starting to see that you CAN have a cake and eat it too. Let's see how to [setup](./Setup.md) this.
