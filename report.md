![image](https://github.com/foukara/report.md/assets/170763146/fcd36e28-8301-4826-91e6-2c09ab40fed1)Detailed Methodology & Walkthrough
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

The first 8 addresses of the cluster share the same OKX deposit address 0x0d5eA059602029Dda50c3DD96609d086307e2E3A. The rest are linked to numerous addresses of the cluster, multiple times.
```
0x618ee1b1276781cfc7180266aaa737ab8df48518
0x2eeb17c2e810a80e76c37003f0540fd6c75dc236
0x7a7a7930d462b959e5d1b34b0a34ca2452dcb1ab
0xaac186bda1edfe82698265f4e5dee822e2aa2ab5
0x04adcb18c1ebaf21018cef1a7d185d410ddd4df9
0x145aa20fe7f57d43e0395afe5aba3bd5b22e1fd3
0x025fc16c31cba10cdc701326a92a40efeb940335
0x35ebf556bf44fec28f0ceb441644372ed2cedddf
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
0x22586c454cc999fc84ab83b5e343564a23e05a0b
0xd0b3dc955e888ca7ddb89ad7d40d876a4dc66e2d
0x2174f7d4ef23544b40a2132b2de2baab0d926a22
```
![Capture d'écran 2024-05-25 051921](https://github.com/foukara/report.md/assets/170763146/75a28c90-e539-44d2-aaca-afa3b5a1cc24)


The addresses have the same L0 age (date of first L0 interaction), 751 days ago, aswell as similar amount bridge, contract count, number of unique days/weeks/months etc...

CLUSTER 2

The first 13 addresses of the cluster share the same Binance deposit address 0x8fb8f74078965dc68457e7A9518184cE683bD16B. The rest are linked to numerous addresses of the cluster, multiple times.
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


CLUSTER 3

The first 16 addresses of the cluster share the same Binance deposit address 0x4b935DB63500Ac5E54Adf49AF7B70C111D4734b7. The rest are linked to numerous addresses of the cluster, multiple times.

```
0xc543ab34899698dcf3e381c8e42c839857578437
0x5a132a762d55d28d762750a8982fc093dafce2c1
0x1407b89162542385b024612e5f3203a544551049
0x827a56edd16ccdfd37950917c7668ae3a5a322ba
0xf19947a12cd486733f555409a2baadec7d9a407a
0x36ada9506f58e3783b384826d8790cb386bef809
0xf60e776444db3d107805b81f3df21fa850a28816
0x63aa5ef4dc2ea1629dae274a4b64a765bcecbc88
0xe652fb90681f45b65900040c507d47cc7023ac4b
0x7595c793f3da6c1a99cd8ec0b4ac62787b967c06
0xdd4c0012af491dcb9839153f24952e60bc2a98bf
0x672cebb82cc1517118bb02935c2c0c4a04b6afd2
0xb7c8fd9b644830a3e5c93cd6d66501fb91ae6ee2
0x6cc1cd6d45c219778b934a969d873648f5c6c389
0x019e397d9f05ff5079e9b16bfc5f4281bc63b569
0xecb6add414bd2dc77906a0335b904f25490e9921
0x024cfd43ba4eb4d215b21ad364fa8ccff560802d
0x591babe0d235585a8e6c5b200820aa51b3152e29
0x1f55f2af3f4db9ec65e05656b6f5daf146b6d1f1
0x40db042211174888bd3803683fff52b139e1cc38
0x681a522351bb494c2139bbec4ed5c9e6909fad91
0xa575d5a49dbd5806f07ecfeb49953e9ace6a60f9
0x1ebcedecee39a5dab3a1ea51280eec5972964068
0xbb764faf49fd7e77d31ad08cd2581c6252896e7f
0xdf99a7dfcb51e82fcfff30e99799759bd2090657
0x810b2164839d435bb45d49359806fee60a4711ba
0xef7d928eb9331461f5236789aad57f48c96dffa6
0x6c9474ab1b6657287eddf9e0fc38186d472612e0
```

![image](https://github.com/foukara/report.md/assets/170763146/a6469402-c99f-423b-ade3-db5e9f2adf45)

The addresses have the same L0 age (date of first L0 interaction), 414 days ago, aswell as similar amount bridge, contract count, number of unique days/weeks/months etc...

Details

![image](https://github.com/foukara/report.md/assets/170763146/d7970f41-5be3-4579-b6f8-369ff7cca016)

![Capture d'écran 2024-05-27 125954](https://github.com/foukara/report.md/assets/170763146/0666397b-c3af-4750-abef-8d953bb87840)
![Capture d'écran 2024-05-27 125908](https://github.com/foukara/report.md/assets/170763146/ce318c66-bea0-4a21-995f-1f4ac37969e2)
![Capture d'écran 2024-05-27 130100](https://github.com/foukara/report.md/assets/170763146/4b5e85d1-4099-4210-b3e4-4d13a6fff485)
![Capture d'écran 2024-05-27 130036](https://github.com/foukara/report.md/assets/170763146/31ece054-f990-435f-a6e3-f4560ec1d303)
![Capture d'écran 2024-05-27 130014](https://github.com/foukara/report.md/assets/170763146/a4ca5a11-6520-4b29-b282-5e6c177f1f7f)

The addresses of the cluster share the same on-chain activity. For example, they all used the Linea bridge multiple times in the same day timespan to bridge ETH.


CLUSTER 4

The first 23 addresses of the cluster share the same Binance deposit address 0x21EdE3eed957dB25eFB92efab6d01D38D3D71C0B. The rest are linked to numerous addresses of the cluster, multiple times.

```
0x7fb1d49be4ee757afc9d453093ed27f8c58cb541
0x2d027f8921fb675f0e3a9fc12bbb69848eb3c4e4
0x25c8a47129746b23481d8ca3fc8b1fd4e3a4e621
0x63f05818c675ae9542e679129299bf919a5f2e19
0x02d4dd1f267a4a55526cb71994f88c4e2ac7e8f9
0x1dc4fabda38c8cff4c547fbb9dbad24d86df234e
0x5d265b6946b0e43f130108606c2a177fe362b792
0x41f73466b30c2fce024ad14231d10579c52d31aa
0xf750303e9887a405b5e7e9033ca70818ea4d14e5
0x4df5d26454c83f843431e30c75f5f47bb944bb66
0x42b3368ce67c09825db437833dbfd94a9c72b196
0x32ab22af29fa6d887523ed4d294eebc710a59465
0x2c9aaf3915e15d8bc31e5efafccbebd19de5e6d5
0x61d7910148a48124d47fea79ddb96ce60fb72547
0x0fdd855cfdfd2be66c3603af112a50ebd3d72fd7
0x80e718301097e5efd5d151a7a939d623a1e9f403
0x10495bfeac15fabeb51c37703b28a424fd9ae397
0xceee95540348ef4befd72a94348bf6e7a8d17fd4
0xe819a2b7f73602e37569b09b621b7cbcc5cf230b
0xad055dab70c3623e42986e7566509061b066e6cb
0x6d9d33f6a474459f69e1899fed9dae876bc21dbc
0x7114fddf2f16a737726267990ccd9937f1d03e9d
0xfbe737d11a22fe02a6b725bb4ff394168dae84b6
```

![image](https://github.com/foukara/report.md/assets/170763146/cb45fe0e-3923-4045-940b-253170320a47)






