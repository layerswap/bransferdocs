# Bransfer Docs Home

Welcome 👋 to the offical docs for Bransfer, the software that helps you save (money and time) on exchange to exchange crypto transfers.

## What? How?

You create withdrawal from one exchange to another. Exchange takes your withdrawal, validates a bunch of stuff, uses a bunch of cryptography to compose valid blockchain transaction and pushes it to blockchain network. After that miners pick up your transaction. They start mining and mining, then after they finally find those `00000...` in the block hash they publish the block with your transaction.  But, as if that was not enough, you still have to wait for a couple of more blocks to get mined, and only after all these your transaction can be confirmed. Still have to wait for another exchange to pick up that transaction from blockchain and credit it to your account.

![Standard withdrawal](/assets/standard_withdrawal.png)


The question we ask is, is this what we really wanted guys? Ok, this is some cool stuff - cryptography, decentralization and all. But you are in centralized exchange and you want move your crypto to another centralized exchange. Why do you have to go through all this complicated process, pay insanse amount of fees and wait for your transaction for insane amount of time? 

Most of exchanges has internal transactions. When you create withdrawal from one exchange account to another one in same exchange. This is done almost instantly and with 0 fees as these transactions doesn't go throught blockchain. ([example Binance](https://www.binance.com/en/support/articles/360037037312-How-to-Make-Internal-Transfer-within-Binance)). 

![Bransfer withdrawal](/assets/bransfer_withdrawal.png)

Let’s take a closer look at binance and huboi. We create institutional accounts in both of them. Whenever you want to withdraw from binance to huobi, you withdraw from your binance account to our binance account. We detect this transaction and create withdrawal from our huobi account to your huobi account. As you can see it yourselves, both transactions are internal. You don’t have to pay network fees (just throw a coin to your witcher) and you almost don’t wait, those transactions are made nearly instantly. 

We ❤️ crypto as much as you do (except one nerd). So don't immediatly start blaming us (blame only him). We understand that this is not so called crypto-way. We understand that we are centralized institutaion which is against decentralizaiton. We are horrible. Ok. But the issue still remains, there are centralized exchanges and we for no necassarity pay a lot of time and money for e2e transactions.

You are probably starting to see that you CAN have a cake and eat it too. Let's see how to [setup](./Setup.md) this for you.
