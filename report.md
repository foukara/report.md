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

CLUSTER 2

The first 13 addresses of the cluster share the same OKX deposit address 0x8fb8f74078965dc68457e7A9518184cE683bD16B. The rest are linked to numerous addresses of the cluster, multiple times.
```
0xf0f1a72e52a0f0bc942e479ad368a86809517c17
0xaedde46485d2495925354d41e25ae5df2ad6d3de
0x89ceb77baa74200f674943cd21183a558ccced18
0x8df1ce48340b427434ba9914f63550ab3df549ff
0xb4b1210234044b675cd5fc9bbc38a34417e377f5
0xcd5936b62546cc1d241f075ea4ba53399bf7b5e9
0x31cfd60afef09c41cf4ec3e4c0a95c6f87c58441
0x8f94c8f2464f33401cf21638db9a39fe04132d53
0x01b2a85bf81aa68ff11a9ec0b873cb5f13a996da
0xee935f45a6b4e2bf50b59ee217676fdc2261f9ff
0xa13b855b065e2510213a2e845b1a9a7741cf578a
0xaee7883f1f9b38cc2e0af64d432e5bff63c0b38c
0x8dfc868e2d54f9c6b3d2c6b0f4da5f5df118157f
0x73788a96af74eee9dbbcc31c47069062122b7833
0xd637d4174c30d42df62143df01945c4eef1a082b
0xf62cd2f726f26354e4e9485870c95efaaa83c374
0x50015ce22e30fe5a088592bd6838b725e8009fa8
0x49247167ec065d0b2e5673093fe7f2f290650430
0x710c9d12369a8dd40c058938beffcee294c2d999
0x4d3fccdce0ce00502d4e258960857fb3747a3dec
```

![image](https://github.com/foukara/report.md/assets/170763146/c9c93e6e-a29d-4a0a-8656-778004101997)

The addresses share the same activity on the chain. They execute the same transaction at the same time to bridge and exchange funds between 15 wallets. For example, they all supplied the same amount of USDT (around $2,000) on Harmony Bridge between 24/08/23 and 25/08/23 to build volume.

Details
```
![Capture d'écran 2024-05-27 034259](https://github.com/foukara/report.md/assets/170763146/f9bc1188-ab17-4d3d-a1d4-ba136370cf90)
![Capture d'écran 2024-05-27 034356](https://github.com/foukara/report.md/assets/170763146/ccb991e0-7056-496e-a7fb-7705bd069b8e)
![Capture d'écran 2024-05-27 034428](https://github.com/foukara/report.md/assets/170763146/c4d72b7d-9f0a-485c-95b6-c50c6d381926)
![Capture d'écran 2024-05-27 034446](https://github.com/foukara/report.md/assets/170763146/630c0300-3308-4d0f-bd03-5c80263d2fd0)
![Capture d'écran 2024-05-27 034512](https://github.com/foukara/report.md/assets/170763146/8798a7bf-6f1f-4f9c-b0b3-a14a1fce8b33)
![Capture d'écran 2024-05-27 040325](https://github.com/foukara/report.md/assets/170763146/3699620f-90e4-4bfd-aa90-5cf4aa74c19d)
![Capture d'écran 2024-05-27 040405](https://github.com/foukara/report.md/assets/170763146/5fa7e96d-7e22-4f57-9cd9-c700352ae895)
![Capture d'écran 2024-05-27 040426](https://github.com/foukara/report.md/assets/170763146/8b1168e5-adf0-45d0-85cb-bbc477fd8f84)
![Capture d'écran 2024-05-27 040751](https://github.com/foukara/report.md/assets/170763146/c6618fdc-b759-4bfa-b83e-77d0f6543707)
![Capture d'écran 2024-05-27 041243](https://github.com/foukara/report.md/assets/170763146/3e90e5e2-05cb-4953-9de8-ff35926509e4)

The cluster shares the same CEX deposit address and exhibits identical on-chain activity simultaneously, it is undoubtedly a sybil operation.

