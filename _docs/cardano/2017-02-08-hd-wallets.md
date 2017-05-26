---
layout: default
title: HD Wallets
permalink: /cardano/hd-wallets/
group: cardano
---
[//]: # (Reviewed at dec0d911d6c4beb8e708ed4076f832ff871f6125)

# Cardano SL HD Wallets

This is an overview of HD wallets in Cardano SL. HD (Hierarchical Deterministic) wallet is
an improved wallet for Cardano SL.

Each wallet contains `N` _accounts_. You can think of an account as of a conceptual part of the wallet.
It's possible to use each account for different payment purposes. Each account has an index.

An account, in its turn, contains `M` _addresses_. Each address is using to receive and send payments
for an account this address belongs to. This is example of an address: `19Fv6JWbdLXRXqew721u2GEarEwc8rcfpAqsriRFPameyCkQLHsNDKQRpwsM7W1M587CiswPuY27cj7RUvNXcZWgTbPByq`.

It can be shown by the following scheme:

~~~
wallet
    |
    `- account 1
    |    |
    |    `- address 1
    |    .
    |    `- address M
    .
    `- account N
~~~

## Workflow Example

After the new wallet `W1` is created, it doesn't contain any accounts. At least one account should be added
to receive and send payments.

To receive a payment to account `Acc1` we have to provide an address `Addr1`. This address can be used
to receive more than one payment.

To send a payment to another wallet `W2` we have to send money from `Acc1` to an address in account in
wallet `W2`. Suppose we have 100 ADA and want to send 10 ADA. After thransaction was created remaining
90 ADA will be transferred to a our (newly generated) address `Addr2`.

Money can be transferred between our accounts `Acc1` and `Acc2`.
