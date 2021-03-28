---
title: Auto
parent: Setup
---

# Auto Setup

With auto setup you only have to pass step by step configuration in Bransfer app and forget about it once and for all. Every time you need to withdraw to the address provided by Bransfer, money will automatically be forwarded to the destination exchange. All you have to do is connect  both source and destination exchanges in Bransfer app by providing *read only* API keys. After that you need to create TransferFlow (which is a link between exchanges), select source and destination exchange as well as the crypto asset you want automatic withdrawals for, after which Bransfer app will return you to the address in source exchange which can later be used for withdrawals. 

ATTENTION! Do not add non-read only API keys. We use API keys only for reading data. 

We use Source Exchange API keys to match deposits that came to our address from a certain user who requested withdrawal. And Destination Exchange API keys are used to find the address to which withdrawal has to be done in destination exchange. 

Let’s start with generating API keys in both exchanges. 
- Login to Your Huobi Account > Api Management > Generate API KEYS
- Login to Your Binance Account > Api Management > Generate API KEYS
- Now we need to activate these both exchanges in bransfer dashboard. 
- Go to Exchanges section and for each exchange put corresponding API keys. 
- Go to Bransfers section and create new Bransfer. 
- Select Source and Destination Exchanges and the asset you want to withdraw. 
- Then you will be provided with intermediate wallet address in source exchange which you can use for withdrawals. 

Copy provided address and now whenever you want to withdraw from Source Exchange (in this example binance) you have to withdraw to the provided address. After that we will detect this transaction and automatically do withdrawal form our destination exchange (in this example huobi) to your huobi account’s corresponding the address of the asset, which we will get using your API Keys. You can do as many withdrawals as you wish. Everything will be done automatically without any user interaction. 
