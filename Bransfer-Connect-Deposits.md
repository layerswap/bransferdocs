---
title: Bransfer Connect Deposits
parent: Bransfer Connect
has_children: true
---

# Overview

# Create Account

[Register](https://connect.bransfer.io/auth/register) your Bransfer Connect account and confirm email.

# Create Application

[Create application](https://connect.bransfer.io/application/create) which is going to accept Bitcoin deposits.
 
Provide your application name and what Currency you want to accept.

# Exchange Activation

Go to Exchanges Tab and activate the exchanges from where you want to accept payments.

Click Enable and entery your read-only API kes from that exchange.


# Widget

Copy your widget code, from Integration Tab, which should look like this:

```
<button type="button" onclick="window.open('https://connect.bransfer.io/Widget/Index/{ORGANIZATIONID}/{CLIENTID}/','popUpWindow','height=650,width=400');">Deposit with Bransfer</button>
```

* ClientId should be unique id, for example user id in your system


# Webhook

In Integration Tab, put your Webhook and click Save. After which Copy your Secret and store it securely.

After detecting deposit we will send you this json as POST request to your webhook:

```
{
  "DepositId" : "95cf2fb1-a20c-4bda-afd7-7b81dedee20d"
  "ClientId": "1234567",
  "Amount": "0.002",
  "Network": "BTC",
  "Asset": "BTC",
  "Exchange" : "Binance"
}
```

# Webhook verification

1. Get the signature from the `X-Bransfer-Webhook-Signature` HTTP header.
2. Get the timestamp from the `X-Bransfer-Webhook-Timestamp` HTTP header.
3. Compose payload
```
// C# example
var payload = $"{model.ClientId}{model.Amount}{model.Network}{model.Asset}{timestamp}";
```
4. Verify Signature
```
// C# example using EllipticCurve
var decodedSignature = Signature.fromBase64(signature);
return Ecdsa.verify(payload, decodedSignature, publicKey);
```