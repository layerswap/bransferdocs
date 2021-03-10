---
title: Auto
parent: Setup
---

# Auto Setup

With Auto Setup you just do configurations in bransfer app and forget about it. Every time you do withdrawal to the address that bransfer provided we will forward money to destination exchange. Automatically. You connect both source and destination exchanges in bransfer app by providing read only api keys. Then you create **Bransfer** which is link beetwin exchanges. You select source and destination exchange aswell as crypto asset for which you want automatical withdrawals. After which Bransfer app returns you the address in source exchange, which you can use to withdraw amount to it.

CAREFUL: Don't add non-read only API keys. We use API keys ONLY for quering data.

We use Source Exchange API Keys to match deposit that came to our address with user who done the withdrawal. And we use Destination Exchange API key to find address to which to do withdrawal in destination exchange.


1. Go to Exchanges section.
2. Add Exchange integrations.
3. Go to Bransfers section.
4. Create Bransfer.
5. Done!
