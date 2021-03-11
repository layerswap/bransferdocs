---
title: Auto
parent: Setup
---

# Auto Setup

With Auto Setup you just do configurations in bransfer app and forget about it. Every time you do withdrawal to the address that bransfer provided we will forward money to destination exchange. Automatically. You connect both source and destination exchanges in bransfer app by providing read only api keys. Then you create **Bransfer** which is link beetwin exchanges. You select source and destination exchange aswell as crypto asset for which you want automatical withdrawals. After which Bransfer app returns you the address in source exchange, which you can use to withdraw amount to it.

CAREFUL: Don't add non-read only API keys. We use API keys ONLY for quering data.

We use Source Exchange API Keys to match deposit that came to our address with user who done the withdrawal. And we use Destination Exchange API key to find address to which to do withdrawal in destination exchange.

Let's start with generate API keys in both exchanges.

Login to Your Huobi Account > Api Managemtn > Generate API KEYS
![Huobi API Key](/assets/hobi_api_key.png)

Login to Your Binance Account > Api Managemtn > Generate API KEYS
![Binance API Key](/assets/binance_api_key.png)


Now we need to activate these both exchanges in bransfer dashboard.

Go to Exchanges section and for each exchange put corresponding API keys.
![Exchanges](/assets/bransfer_exchanges.png)


Go to Bransfers section and create new Bransfer.
![Create Bransfer](/assets/create_bransfer.png)
Select Source and Destination Exchanges and the asset you want to withdraw.

Then you will be porvided with intermediate wallet address in source exchange which you can use to withdraw.
![Bransfer list](/assets/bransfers_list.png)

Copy provided address and now whenver you want to do withdrawal from Source exchange(in this example binance) you have to do withdrawal to provided address. After which we will detect this transaction and automatically do withdrawal form our destination exchange(in this example huobi) to your hobi accounts corresponding asset's address, which we will get using your API Keys. Everything Automatically. You can do as many withdrawals as you want. Everything will be done automatically without any user interaction.
