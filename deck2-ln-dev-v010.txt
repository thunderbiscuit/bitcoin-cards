## 101.
Why do we say that in lightning, you need to "actively defend your channels"?
---
Because all channel states are valid from the network's point of view. The only thing making past states invalid is the fact that if they were broadcast by your counterparty you could steal all the money for a window of time, but that requires active monitoring for past states to be broadcast and proper action to claw funds back. If you're not "defending" your channels, any channel partner can broadcast an old state and get the funds this past state stipulate.
=====================










=====================
## 102.
The initial idea of the Lightning Network was proposed in {{2015}} in the groundbreaking paper The Bitcoin Lightning Network: Scalable Off-Chain Instant Payments, by {{Joseph Poon}} and {{Tadge Dryja}}.
=====================










=====================
## 103.
When value is exchanged on the Lightning Network, we call this a {{payment}} as compared to a {{transaction}} on the bitcoin blockchain.
=====================










=====================
## 104.
Why does transaction malleability break the Lightning Network payment channels idea?
---
Because in order to build and broadcast a funding transaction, you need a refund transaction to be signed so that you have assurance you'll be able to get your funds back if your counterparty goes offline. But this refund transaction needs to sign a transaction that spends an output that isn't yet in the blockchain (the funding tx multisig output), and so it needs to be constructed with a particular outpoint, but if you have transaction malleability that outpoint can change under you and the refund transaction would then be invalid.
=====================










=====================
## 105.
What is described in BOLT #1?
=====================








=====================
## 106.
What is described in BOLT #2?
=====================








=====================
## 107.
What is described in BOLT #3?
=====================








=====================
## 108.
What is described in BOLT #4?
=====================








=====================
## 109.
What is described in BOLT #5?
=====================








=====================
## 110.
What is described in BOLT #5?
=====================








=====================
## 111.
What is described in BOLT #6?
=====================








=====================
## 112.
What is described in BOLT #7?
=====================








=====================
## 113.
What is described in BOLT #8?
=====================







=====================
## 114.
What is described in BOLT #9?
=====================








=====================
## 115.
What is described in BOLT #10?
=====================










====================
## 116.
What is described in BOLT #11?
====================







=====================
## 117.
What is the idea behind lnurl?
=====================








=====================
## 118.
What is the idea behind lnurl-auth?
=====================








=====================
## 119.
The lightning network relies of 4 types of transactions. What are they?
---
1. The funding transaction
2. The commitment transaction
3. The closing transaction
4. The penalty transaction
=====================








=====================
## 120.
The default port for a Lightning network node is {{9735}}.
=====================








=====================
## 121.
What is the format for full Lightning node identifiers?
---
```
nodeID@ipaddress:port
```
=====================







=====================
## 122.
What's another name for the refund transaction?
---
The commitment transaction.
=====================








=====================
## 123.
What's another name for the commitment transaction?
---
The refund transaction.
=====================








=====================
## 124.
Before attempting to create a channel with Bob, Alice will need to add him {{as a peer}}.
=====================








=====================
## 125.
If Alice wants to open a channel with Bob, what are the first two messages their nodes will exchange?
---
1. `open_channel`
2. `accept_channel`
=====================