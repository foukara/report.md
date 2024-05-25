Detailed Methodology & Walkthrough
Data Collection:

Hot wallets and gas suppliers from major centralized exchanges (CEX) like Binance, Coinbase, Kucoin, Bybit, and OKX were gathered using blockchain explorers.
Using a Dune SQL query, approximately 2.5 million CEX deposit addresses were collected. These are the addresses where users send assets to deposit into a CEX.
Filtering and Clustering:

With a Dune Dashboard, CEX deposit addresses that received funds from at least seven addresses regularly interacting with Layer Zero were filtered.
Clusters of active Layer Zero addresses sharing the same CEX deposit address were created, ranging from 7 to 300 addresses.
Larger clusters were formed using a script, incorporating addresses that interacted with cluster addresses but not with the CEX deposit address. An address needed to be directly linked to at least four other cluster addresses to join.
Clusters with fewer than 20 addresses (including the CEX deposit address) were discarded.
First Layer of Detection/Proof:

This automated process identified clusters with addresses sharing the same CEX deposit address, linked to at least four other cluster addresses.
Despite being automated, this layer has a small percentage of false positives due to multiple interactions and common CEX deposit addresses.
Second Layer of Detection/Proof:

Each cluster underwent manual scanning to remove false positives and add on-chain arguments to the cluster description.
On-chain arguments included executing the same transaction at the same time with the same amounts, similar transaction patterns for Layer Zero activities, etc.
Resources used: LayerZero Scan, Dune, Debank, Arkham, Etherscan, among others.
This manual process, though time-consuming, ensures the detection of Sybil clusters and minimizes false positives. It also demonstrates thorough verification beyond a mere list of addresses.
Screening Across Blockchains:

Activity was screened across 14 blockchains:
Ethereum (endblock 19757726)
Optimism (endblock 119326917)
BSC (endblock 38236464)
Polygon (endblock 56379454)
Arbitrum (endblock 205653169)
Gnosis (endblock 33677943)
Linea (endblock 4059728)
Scroll (endblock 5184468)
Zksync (endblock 32656745)
Moonbeam (endblock 6045324)
Moonriver (endblock 6637617)
FTM (endblock 80127182)
Base (endblock 13709885)
Celo (endblock 25273962)
Arkham Diagrams:
Arkham supports only 7 out of the 14 blockchains used in this report, leading to occasional missing links in Arkham diagrams.

Conclusion:
The combination of automated and manual detection processes, thorough screening across multiple blockchains, and the use of various resources ensures high accuracy in identifying Sybil clusters with minimal false positives. This rigorous methodology underpins the credibility and reliability of the findings presented in this report.

Table of Contents
Independent Clusters and Descriptions
Since each cluster is independent and includes its own description, the following sections have been consolidated for clarity.

Cluster Details
This section provides a rotation of the list of addresses within each cluster and its description. It includes:

The CEX deposit address shared by some of the addresses
An Arkham diagram
The second layer of detection and proof

Reported Addresses & Description
CLUSTER 1

The first 9 addresses of the cluster share the same OKX deposit address 0x0d5eA059602029Dda50c3DD96609d086307e2E3A. The rest are linked to numerous addresses of the cluster, multiple times.
```
0x4b1f10157951a7b72640e5b33d53d9dbea049b2f
0x13e65d6a92c092da14046c332a7c89e2f35cf317
0x029c46bec4e4b43d363b70f59ef50de36020d51f
0x964ada0e8a30764beb397f1545c2541fe50df173
0x8b2b481e9c0acfbd3b1b1fde296e59abca5ee716
0xd41a74e28be2f5b133f4c7f6f97f8512ee83ea6e
0xdf70127b89a6b6c6c8e241f1bb409a43c3d74845
0xc4b57a09d780a9b7f191a95e97bf8eeb436fdda8
0x5f0868b8241cafd908faec01fd0c1143086ab570
0xfcd0845cbac7e7af231573cdc8767a11e837a868
```
![Capture d'écran 2024-05-25 051921](https://github.com/foukara/report.md/assets/170763146/75a28c90-e539-44d2-aaca-afa3b5a1cc24)


The addresses have the same L0 age (date of first L0 interaction), 751 days ago, aswell as similar amount bridge, contract count, number of unique days/weeks/months etc...
