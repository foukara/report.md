Please note that all cluster of that report are independent and have their very own manual description & argumentation.
backup github to avoid raids : 

# Detailed Methodology & Walkthrough

After gathering as many hot wallet addresses and gas suppliers for several centralized exchanges (CEXs) such as Binance, Coinbase, Kucoin, Bybit, and OKX using blockchain explorers, a simple Dune SQL request was employed to collect around 2.5 million CEX deposit addresses. These are the addresses where users send assets to deposit into a CEX.

Using Dune Dashboard again, I filtered these CEX deposit addresses to identify those that received funds from at least seven addresses that regularly interacted with LayerZero (using an unofficial Dune Dashboard).

Clusters of 7-300 active LayerZero addresses sharing the same CEX deposit address were formed. A script then expanded these clusters by including addresses interacting with the cluster addresses but not directly with the CEX deposit address. To minimize false positives, an address needed to be linked to at least four other cluster addresses to join. Clusters with fewer than 20 addresses (21 including the CEX deposit address) were discarded.

This initial detection/proof layer is fully automated, leveraging scripts to create clusters. Although these clusters are less common due to the requirement of multiple interactions and the common CEX deposit address, a small percentage of false positives remains.

The second detection/proof layer involves manual verification. Each cluster in this report underwent thorough manual inspection to remove false positives and add on-chain arguments supporting the cluster's sybil nature. These on-chain arguments vary, such as addresses within a cluster executing identical transactions simultaneously with the same amounts, or showing similar transaction patterns for LayerZero activities. Resources like LayerZero Scan, Dune, Debank, Arkham, Etherscan, and others were extensively used.

This manual verification, despite being time-consuming, ensures a high accuracy rate by minimizing false positives and demonstrating that the report is not merely a dump of addresses. The combination of automated clustering and manual verification, along with the consistent use of the same CEX deposit address and similar on-chain activities, provides robust detection with minimal false positives.

The activity predating the snapshot was screened across 14 blockchains: Ethereum (endblock 19757726), Optimism (endblock 119326917), BSC (endblock 38236464), Polygon (endblock 56379454), Arbitrum (endblock 205653169), Gnosis (endblock 33677943), Linea (endblock 4059728), Scroll (endblock 5184468), Zksync (endblock 32656745), Moonbeam (endblock 6045324), Moonriver (endblock 6637617), Fantom (endblock 80127182), Base (endblock 13709885), and Celo (endblock 25273962).

Lastly, please note that Arkham diagrams in this report may often lack links, as Arkham only supports 7 out of these 14 blockchains.

# Reward Address (If Eligible)


0x7BA28B2bcD582f56f9B517c0228FF1AB3948557F
This is a fresh address.


# Table of Contents

<details>

1. [Cluster 1](#cluster-1)
2. [Cluster 2](#cluster-2)
3. [Cluster 3](#cluster-3)
4. [Cluster 4](#cluster-4)
5. [Cluster 5](#cluster-5)
6. [Cluster 6](#cluster-6)
7. [Cluster 7](#cluster-7)
8. [Cluster 8](#cluster-8)
9. [Cluster 9](#cluster-9)


</details>


As the cluster are independant and a description comes with every cluster, the two following sections have been regrouped.

This following section is an rotation of the list of the addresses of the cluster and its description: the CEX deposit address some of the addresses share, an Arkham diagram & the second layer of detection.



# Reported Addresses & Description


## CLUSTER 1


The first 10 addresses of the cluster share the same Binance deposit address 0xd2E1cC562786cE8d803128FD8710B79CCCd28260. The rest are linked to numerous addresses of the cluster, multiple times.


```
0x385c0a94802704784331ef5f76208fb918ab3667
0x909e19174a5aa7a3d2aedccfc6e05e0c64fc5f5d
0x3e73311aa4e71af0f5472765fd334bb32f6ff916
0x88632307d47b660f03e376536c7003581c07999a
0xabf5b2f259c3acef7ac0672d2e1851614f6b9a5d
0xc7c7b46c9232b208a8bc43540f42e794086d9881
0x397a5c10c18039676cec523fb509b9ba01280d21
0x79a8874c761b9982ee4d150ebc707846a9d88de6
0x443f33f63de9094f7fcd6f39f1540fe4412641d5
0xad76adfff1668d2bb3c34f8455e13330b54f0444
0x4c4a3c846d5fc34ccfa9dc7955ef6310ef0db19e
0xd0f02cb782fba0f7dbca1eccfcb192b7cf007d91
0xdf99e6d56553a2763bbf2e1c32a44efc05355bf9
0x3b97eb72be539d3cbe4759be7daf001cb8d040df
0x3afb126adb1d5db00aee3e21482fe17198086f66
0x627f4ae1f83871bc503ee2a6349e420a750e2e4b
0xada85f3a8c31d7f22b1db90a514a6a3182837558
0x13976bb80460cf989544c512fa2a04b11c3e1889
0x257ed1ee5b7ae4eceb6f1818829bab8917894944
0x35a35695f3111733df39d99806c68d6be8bc3338
0xee58e3f21ebf1bac5a1bef2f29dd9930a7c78e97
0xf90895702499cd18409e7fd19ba712dd331415da
```

![Capture d'écran 2024-05-25 011418](https://github.com/99mitch/sybil-report/assets/163365834/28c0c1f9-0bb8-4ed3-a865-0a2b170461b2)



The addresses all have the same on-chain activity. For example, the 29/04, the same transaction was made nearly at the same time for 10 of the adresses: interaction with mintCube.

<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/15732be6-0a48-47ee-ac54-e70c6e052723)


![image](https://github.com/99mitch/sybil-report/assets/163365834/4afda5da-ea70-45c7-8249-a0cc66b5335d)


![image](https://github.com/99mitch/sybil-report/assets/163365834/747f68d4-f579-4fc2-814d-40ea06845150)


![image](https://github.com/99mitch/sybil-report/assets/163365834/e129ce0c-7e8b-4b58-9714-e48cafa41624)

![image](https://github.com/99mitch/sybil-report/assets/163365834/1a8995e8-04eb-4d74-8918-dd7d6e1fba49)


![image](https://github.com/99mitch/sybil-report/assets/163365834/d1fa922c-b48d-4064-bb72-0497a51419ce)


![image](https://github.com/99mitch/sybil-report/assets/163365834/ee64673b-c67f-4311-a9a0-a1a28c0b57a6)


![image](https://github.com/99mitch/sybil-report/assets/163365834/df5e77f7-57ab-4662-9f98-0ec3a7974d03)

![image](https://github.com/99mitch/sybil-report/assets/163365834/5e51236f-1db4-4d7c-bb95-22df12c28e47)

</details>

The addresses also all have similar scam tx recognized by debank.

The address share the same CEX deposit address, are part of a cluster with multiple links between one another, and have the same on-chain activity. This is a big scale sybil operation, probably the result of scripts.

## CLUSTER 2

The first 10 addresses of the cluster share the same Binance deposit address 0x70D4282501F8951FeDe458ac53B7D4BBC5360483. The rest are linked to numerous addresses of the cluster.

```
0x237ea6a3840e895eec42bb2c7343d10c097db483
0xb1c6b51cc745665740e77a37237ac506e1a7a179
0xdf49886fe8f44f1358d30654d86c3b418d949fbe
0x16fcd2c7a8d96e1f91e167d34db78f7f0db8ac7a
0x6418122a235d6e7831aec936e79e1fd12d51ad6c
0x2e2a422972472d9bf30ffe1513c4367f7ea20038
0x40e592a8f5c967ac8cc00931e58e3398588b0d97
0x4fe78dee13b94872de53ba4c65dd19dbd7da13db
0xf5918270511997b484d592a3d7b89798fb348007
0xdc2ca72397afb38b72294e658083c0a794bf68d5
0xdffba37790141b5fe20146542834157cd8ad78c4
0xbeb2e566eec5f05cf16cf9112768c21fab0c8db9
0x0af322fffb89b878828211bdc9d4be874cc7017f
0xb4eaa1996ab41f0502cb974bc7154128269d58d3
0x316072ccbeee4f504a4030f9ce3561459b205868
0x2bc9b27433846d505c75cd9bafaea5e6839d6bb9
0x36e60f1f63a158ef441726c5a2ef84a75857c962
0x356cc8ead33d302bed83f5fb62fd01e6bde29b2b
0x60bd18e1bc4dd3f3cb5ba92b436bbe0cf5d0db0c
0xccf302607b73fa3142cbbca11ad8eb8cb5d538ec
0x981c796da09805f3dc54124ec397bac3cf6311c8
0x8043088c341b6b8e906a415f2056a81e417f61df
0xc749a97d4bd68b042e60cf6d39dd40b33824a997
0x1163d2edd37bab505ce520b54554393155583f88
0x1f55f5508dc75185d7d54ef839208ed7a3c4ca8d
0xded2d3916455a840fbd012cb025f82ff23b1de14
```

![image](https://github.com/99mitch/sybil-report/assets/163365834/4ff78058-88c7-4776-8571-b1cd7ccc4ffc)

The addresses have the same on-chain activity. Here we can observe the same interaction with Galxe approximately with the same timespan :

<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/1cde080e-db01-4c02-b223-519d87e1c145)
![image](https://github.com/99mitch/sybil-report/assets/163365834/57678fda-4acf-4ab4-982f-9b9c1f0a2b5f)
![image](https://github.com/99mitch/sybil-report/assets/163365834/7bee2bbb-66c1-4346-bf34-1cd96bea616c)
![image](https://github.com/99mitch/sybil-report/assets/163365834/3438de28-37de-4e52-b013-4ffcdf30bff5)
![image](https://github.com/99mitch/sybil-report/assets/163365834/b4faaac4-c6a3-41da-9031-d87d217a9819)
![image](https://github.com/99mitch/sybil-report/assets/163365834/3362a6b7-c9de-4fe5-b56c-884c69f5893b)
![image](https://github.com/99mitch/sybil-report/assets/163365834/39a8af43-f9e9-453b-9638-a95f2f3ece35)
![image](https://github.com/99mitch/sybil-report/assets/163365834/b08b4afc-df5d-45b0-85a7-c8085d388d71)
</details>


Also here with the interaction done with Stargate and LayerZeroLabs :
<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/fbc493e0-9e97-406d-931d-c193e4dd9252)
![image](https://github.com/99mitch/sybil-report/assets/163365834/9ea80373-83af-49c4-b04f-ae1dd0c830bc)
![image](https://github.com/99mitch/sybil-report/assets/163365834/1c28e484-3a5c-4614-8c29-b560ab1295e8)
![image](https://github.com/99mitch/sybil-report/assets/163365834/ebcdb864-d48e-4c48-b101-269fe3e40161)
![image](https://github.com/99mitch/sybil-report/assets/163365834/942fc77e-91d5-4f2f-b381-78f205808683)
</details>


Cluster + same CEX deposit address + same on-chain activity. Without a doubt a sybil cluster.


## CLUSTER 3

The first 12 addresses of the cluster share the same Binance deposit address 0x90D1574aDA5007266F9D9834Ee413BE1c5488B03. The rest are linked to numerous addresses of the cluster.

```
0x5e0fdd8495eca7d5b966a66aa5f5cac5f441e9a1
0x86b34e94e0307d049ac361c841ca187812f2bef2
0x95b9852a24235b158b0ed29ee8652f565683e1b1
0x0291c611fcf96ae006bfeb0958c5395725473438
0xabdf9b75166a5b647b6dbd1bca1b23407d02fc60
0xd343b83bf66e24a5fef7d3a8d50980ec0d82a945
0xd6de58ce85dda96fe4aa26aad631c5113f4835bc
0x0c04183b92ec26c8bb8e9336e1981377b6da76fe
0x7d1564854e8ba39472848df1855f3caa135e48cf
0x466337057bba53b8113d34729fe65f7872b983bb
0x917d2235fc0390e94a960f7dff262d7c27e9c68f
0xe622188bacf0d299a0daa8575d82185c8862f55a
0x680c15770dd13e463de8cd824079916cc658d9f6
0x3bfc0b688933481af2cc7903fd54d46ffb65d771
0x4e45ca4e00e1b735d6479d343a0cd4b2637768ca
0x70bd865e671044e525b632e08542f59cf7f77e25
0x8ed3e9cfb668f9901b11f48b8520544509d7f287
0x2f21d79099644a9ac8243f2cee5ff95825ff4a11
0x49c7fe58d69b5dbac3b0078b402667319487fb49
0x38db52d222329b65099f58d883e3c54acb5fd597
```

![image](https://github.com/99mitch/sybil-report/assets/163365834/5d04ffef-e475-4f6e-b54e-753d98d362ed)

The addresses have the same on-chain activity. Their L0 is the same, probably due to a script. For example, their latest L0 interaction is the same: Merkly transaction 7 months ago from Fuse, and/or Angle transaction 11 months ago from Gnosis and Celo, for every address. The same patterns happen over and over.
<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/71c11bbe-811d-469e-8172-77f646e833e6)
![image](https://github.com/99mitch/sybil-report/assets/163365834/ef1a949c-d0d7-4b16-8c5e-253de2b3f29f)
![image](https://github.com/99mitch/sybil-report/assets/163365834/f35f3e81-ad47-4d51-b4a7-0576236ed831)
![image](https://github.com/99mitch/sybil-report/assets/163365834/12661caf-ea72-4179-bd8f-8f907dbd8d9e)
![image](https://github.com/99mitch/sybil-report/assets/163365834/e98ef1e1-d521-472a-8171-5c780d5f88b1)
![image](https://github.com/99mitch/sybil-report/assets/163365834/205861d1-c137-4e25-8472-4895c59e1ec3)

</details>

Cluster + same CEX deposit address + same on-chain activity. Without a doubt a sybil cluster.

## CLUSTER 4

The first 9 addresses of the cluster share the same Kucoin deposit address 0xA2847183FDef870736C8ff1681b16a5521CdF9c5. The rest are linked to numerous addresses of the cluster.

```
0x7d0faf59aa2c13be86ea7d08de31881372349ba4
0x7576f8bdc643cdee38fc5f632d5fdd1d13450803
0x29fec76ab80e47c7dc45193f9317567f67758411
0x03adaf38829f8307099db5ea4ddf54919410e2f3
0xc441b17978cbe90671b9d6e4014c323404f3fcc8
0x6816bf1e88c5e0e8d3c45559f8733712f7a1012d
0x5f3582b06b6697fd64e791ab7ace882fe66bc835
0x4bcc72aece459f92b7095dc408a6d646fcce35cb
0x14de75a716c6d75dc8bda719f381b6dbb113e995
0x1bb1296bd63f3c50059f45065ca1ca006be5efe8
0x5770b98e09d69ba91dd68d5cbf20d18826775b82
0xbf18062443c8697ef6b3d3935c2d3a1440642635
0xcb71a8f2387fb6250c445939b61243f0be2f345a
0x5f0b726d9b98a0744fe19141fea973546cd009f9
0xcc1c9902de1a716f8dc926461058444f49a39b50
0xc7d978b8ac926eadd7c79587d3d6cdbe51a967cf
0x6bbce026dc4cee027e8e33b83a44da150a49fea3
0xd9be17108a0783f68464f2aa78510f40ba154f5b
0x01e4683487849ca6002eefe16c5236e867493e30
0xf7756e25081fd36a3a734bef77331581f6d61535
0xbcf633e185089f46badc4920a7f368252b31da2c
0x6bdc7a993085fdd1e77c7c61b8772162fba08cf5
0xd1e00611cc8a8f7bc02ab1748f810e862701c908
0x9824298f695ee57657cb0633444625e806c77770
0x0000bbefde6e3b6613a4f021854cfbd6d3cd66b4
```

![image](https://github.com/99mitch/sybil-report/assets/163365834/bad9b266-4a39-4cb7-b722-bc698ea06bfd)

The addresses have the same on-chain activity. Their L0 is the same, probably due to a script. For example, their latest L0 interaction is the same: Stargate transaction 26 days ago for every address. The same pattern happen over and over.
<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/bc759d2c-7950-4b98-a31c-393b35413c45)
![image](https://github.com/99mitch/sybil-report/assets/163365834/b4d7ee10-a4ad-4a3c-9ee1-1929464b3cdd)
![image](https://github.com/99mitch/sybil-report/assets/163365834/d328064b-63cc-401a-997a-3e2afac49f0d)
![image](https://github.com/99mitch/sybil-report/assets/163365834/8133026b-33ce-4944-beff-f5bc8c4f7149)
![image](https://github.com/99mitch/sybil-report/assets/163365834/4ddb03e6-0dfa-4b20-90b8-58d47408fc42)
![image](https://github.com/99mitch/sybil-report/assets/163365834/2d794417-d693-4ddf-bc21-10823c25f64b)
![image](https://github.com/99mitch/sybil-report/assets/163365834/46c862a8-2c81-4955-a474-648121d7f0aa)
![image](https://github.com/99mitch/sybil-report/assets/163365834/c4433b62-65b9-448e-937e-2b5ac855f984)


</details>

Moreover, They have similar LZ Age (date of first L0 interaction), amount bridged, contract count, interacted source chains, Unique Active Days etc...

![image](https://github.com/99mitch/sybil-report/assets/163365834/ce4d1f51-7a12-4ba1-afb0-328f6e8e58f4)


Cluster + same CEX deposit address + same on-chain activity. Without a doubt a sybil cluster.

## CLUSTER 5

The first 11 addresses of the cluster share the same Binance deposit address 0xA4a3A63efDe3753f3a86986d6E08E046C7353406. The rest are linked to numerous addresses of the cluster.

```
0x5d7adb0d79846fcc2b6ffbda98f33adb4b00f2e7
0x9f45f7f50e90337fa50c625db98ae584bc1dc48c
0x65fc291a2252199a6dfac06fed2e5246db341ac0
0x26914add47df18adbe372fc4d6f8d3ea97e7e063
0x79fb1cbafdf2395980a649a86fd2afe275b0eed6
0x3dc75d5e1693a3c27ba9a54a7de67d34c6694f8c
0x67b98d282aec23fc4d52b41c755f22b31081ffa4
0x65b740a41dba844e4de430095da76972e16f1602
0xe8c907430e1ed83797e0a8bf1eda14a8087cac92
0x7c5b381535b3170043ad444274086123757871d6
0xf38b2abed6c38667a63240678cf84e119041d195
0x082677a0ea5566b3e6b65af9dfb61f17aa7b73d5
0xde009afccce855405e57f4342eb62c9a4520cf6f
0x8a4ad70f227ef77ca371b6eb12445d6d52681850
0x84db1c103066df7b9dd510397c8ade8b0e5999d0
0xaee5666c82df7aad6c7f7e7538e631c9d0c89eb9
0x69848a3b8ed8d1424a846c807a240538f0ff0197
0x136c2b7118beb7bd7981360d36bb5010b5608f25
0xfff84b5e92ac9fe353e2c0fd6ac2e42af390b865
0xaa885b4bc2d2dd326bbe604d55d52421d0a72ea1
0x456c55b4aed43928ff619007e25b847a9939e9cc
0xaa7134be644fa155fc299132633d14fc81018c87
0xa1c55dec3f08fbe6a8b6cf399bbe2d016150eca8
0x7ff34da86a1b03a83e1f021c37b0b4ab6598f212
0x3b11a9a33fb286eb564b387fc7daa8b8b154d949
0x01fabc7e3ee0d830a134f4b744e6fdceb592f97b
0x4568806f725fd5b96950194a87dea09d293bcb3c
0x38c192d6056e8a7b1b91176435eb9b8657689ab8
0x9da9fc9f85c70c029bcb1316cd162ed62a94f506
0x2c6263cc7d914777a12461d622e2edf523885ab5
0xa7a3d484b2229681214d21a08262ebb05b46946f
0x26327d036cc08b93bcb9e475c8450ba8a3225daf
0x3f82dab372a375285e0243583aebd088ee59d625
0x5010e94232f3f2df4b303a759c4a8ed6b24c5309
0xb328cfc34b3dee0e01182826a5405ac306151c36
0xc9315fc369afd5a55689f033b4e6fe90d4da9a9d
0x7078943ba34c0064f8e7ea40c368520e002a4575
0xe8f4fcf52f76f82109327553945250c986c6d0f3
```

![image](https://github.com/99mitch/sybil-report/assets/163365834/94380a0d-8888-4fdb-bb0a-ba693ef92e2f)

The addresses have the same on-chain activity. Here we can observe the same interaction with Stargate approximately with the same timespan :

<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/0e23bc07-7df4-4c90-a33d-6b4db530f41a)
![image](https://github.com/99mitch/sybil-report/assets/163365834/b4d7ee10-a4ad-4a3c-9ee1-1929464b3cdd)
![image](https://github.com/99mitch/sybil-report/assets/163365834/87b53191-272e-45ff-a749-86bc92fd2d6f)
![image](https://github.com/99mitch/sybil-report/assets/163365834/244f686b-ce06-4da9-89c0-82f59bec65d6)
![image](https://github.com/99mitch/sybil-report/assets/163365834/ca229c89-08bb-4ec1-9c02-12ced1e49d65)
![image](https://github.com/99mitch/sybil-report/assets/163365834/fde9558b-3aa2-4fc4-850b-85f4dc72c4b9)


</details>

Moreover, They have similar LZ Age (date of first L0 interaction), amount bridged, contract count, interacted source chains, Unique Active Days etc...

![image](https://github.com/99mitch/sybil-report/assets/163365834/be0c6700-3deb-46df-9615-36002be0f27a)


Cluster + same CEX address + same activity accross +20 wallets to farm airdrop. This is surely a sybil cluster.

## CLUSTER 6

The first 12 addresses of the cluster share the same Binance deposit address 0xDc14Cfa9294d1816781f8CFA04398D95d9aBf675. The rest are linked to numerous addresses of the cluster.

```
0x231466ee5a820e1802081ee4828f6673a400a2a1
0xbdb0884f0a422843f8846869f1909fc6cf921b70
0x0b24b6b5a2b1bac48904fea84b8bd23d16515c5b
0x5a1b39f31e894729217fc10ee7ba1d602a56accd
0xcb43410589a3fb3a2c31e9c6a118af5887d3a64d
0x9668b5b5e5dd787bc84044929727fe8d44a659d8
0xce70dfcb8126f9794c85f857ac5f68b042dad801
0x28784a9d1d45ca2f31da678fd5b3091938b8598e
0x9e16786929eecd46216115adad27dc9b9cca821d
0xddeaa37a75573278fbf9fc51b03bd863db1b63f4
0x735008aeaec303cdc3814bf3a0952a1aac2d7d37
0xaf18c71487eec382c6cc6bf3284a08dcc9a87ce9
0x50b2112ae316630decb1cf170e650b1253decf12
0x542e21321e798724cdcb6bd88024f7eb5439ea48
0x03d91f6df2e871bfdcaff863de3c2a9feaa391e1
0xa656902a2c99fcfa61d6b40d8900f37a4daccf6f
0xe44a5a0d512cc0542c759580c087307c14543cf8
0x00cfc2ee6ba2c77ccb905d2dc795b5e6c10d12b5
0x9c6050375d3e721e9ed127d1f8c0ad58f32ad624
0x203d76528dd0f36ccfc3c400c20baec0c2bb98a7
0x611a0d18c38fad11c2b1f67f3aca76da32682fcf
0x1639baed28d1f76a347e81f92a890064c10105ae
0x51858b79a725a5bf4de8aedbdab006f274578401
0x94cc44233e1c5f5e51f817f88bff610a3ec4fc22
0xf8e164a8121569ee85505491231a3c2c7ab09186
0x2e690239a67c8f0805df0bffc7056ed067d8022d
0xac94be38c5f72783e769feef92eb0e8eed65ba8c
```

![image](https://github.com/99mitch/sybil-report/assets/163365834/080b403d-f6d0-4913-8379-bbe116d91cc5)

The addresses execute similar transaction at the same time to farm airdrop accross planty wallets. For example, they interacted with Stargate back and forth to lock STG with similar amounts during the same timespan.
<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/597076e1-225e-4ed0-a1dc-4978e86cc9c7)
![image](https://github.com/99mitch/sybil-report/assets/163365834/698c67d8-e061-43aa-8680-1e7b830112e9)
![image](https://github.com/99mitch/sybil-report/assets/163365834/2fe4d2e2-14ba-48e8-af27-cbec382e4f7c)
![image](https://github.com/99mitch/sybil-report/assets/163365834/1a3c4833-2630-4c5b-a8d5-34649b6d82c0)
![image](https://github.com/99mitch/sybil-report/assets/163365834/748c1a34-c63a-46d3-876b-5daeed43f8ee)
![image](https://github.com/99mitch/sybil-report/assets/163365834/db5cf645-450b-4cb5-9517-ced30045517b)
![image](https://github.com/99mitch/sybil-report/assets/163365834/6c7ad112-d842-4f82-87c5-17616f5d9ea6)


</details>

Moreover, They have similar LZ Age (date of first L0 interaction), amount bridged, contract count, interacted source chains, Unique Active Days etc...

![image](https://github.com/99mitch/sybil-report/assets/163365834/c2042f32-76b0-4a9f-a97c-344af5f59899)


Cluster + same CEX address + same activity to farm airdrop. This is surely a sybil cluster.

## CLUSTER 7

The first 12 addresses of the cluster share the same OKX deposit address 0xaF2E326D4C89c8e9e59FF170F451ce306cb60D42. The rest are linked to numerous addresses of the cluster.

```
0xa2468ae73dda2aba7ea11ec97d35410e5dddcd84
0x68141d2a9658d1b58592bcdf81b2976e43537b8f
0x4f4c3ab2c02733e65742aec39af49f0ab80dfe15
0xfcb59a8c5d5be3b514ebcbaf71567fd2bd4bffcc
0xea596320baba2112398b281b79aff1a9a6b07656
0x7e79ccc87f08969cdf3e97ad6529ab5a2c0576ef
0x4b15a92c77d290961c99df629b7ab94fca144c29
0x37a213ab3edc49f82674fb98159e3609c6812ec3
0x1b27c88ce8ddac32e5cd4dcbaecf67d4c8fdee49
0x6fa50e6f0027222582080a20149d0bff9a6842ed
0x2c6802060c60162c0bf45e3df533415c49c7c0ba
0x90f044e97d67e7fa450b5fa56d7fd65bdd199c6f
0xe4f15252d4d3d9d8eb740dd6619a3f7d431df3a1
0x24781c9adba5e4ab8aedaf82f1e6a0018f1de350
0xbb41a00fe950fd88fe556343fc4e345f3ef4e1eb
0xfdfd36b8c94c1f36adcf2318d1250434f5c359d7
0x24fd52b9a97ee5fa4bd4d02e2ceb22af3f786d45
0xcf7e9d3136c6b6597eec2c32e5243d815c211422
0xe9ec9f7233862462a1d007b8df12b60a961578ab
0x5ac2affb99437a6bc3a9df539fc3146f029356bb
0x84d31cbfa184746acf08aaf7b5ea95cf50d06f4a
0x7df61326a523ae6370a7c7e70da904d86b006d93
0x61a30247e119daf8b24f507ab81ab421b27b17c3
0x58962f05b8503f3ca1737d52b37e4c96cd1e581d
0x5f6f1a3bea5d366721105338ef0ece97c12b4ae8
0x430bd9aeed2c4e409b8742bc27dcc9df398eafe7
0x672a31d93d2d02fe4c7396a01b0b01e1b6485630
0xe9ffb19109f547e8e9ce546daf29aaefe2ef66de
0x9844820f0e8d6ca6fab74133d820e5864b1e1c19
0xad3454093a99e34990ccafe195091d4f70f50e5f
0xa6790b9829898eb407cbefddd2ea46adb8841ef0
0x4103d2fa741316fa36fea82c446dd256ab543c13
0x113d3a76f43df30c84f14fa168a2d428b29979bc
0x62be51149a6bb9fe7de7ff4ebfa5ab6a461351e2
```

We can observe from the arkham modelization that the adresses are more than linked :

![image](https://github.com/99mitch/sybil-report/assets/163365834/cdda65cc-50e6-4725-b949-28dc156dc84b)

They have similar LZ Age (date of first L0 interaction), amount bridged, contract count, interacted source chains, Unique Active Days etc...

![image](https://github.com/99mitch/sybil-report/assets/163365834/1a1b85ac-2988-40b9-b914-462cf72e8da8)

Cluster + same CEX address + same adresses interactions pattern. This is surely a sybil cluster.

## CLUSTER 8

The first 10 addresses of the cluster share the same OKX deposit address 0xe0e4c1b6Eda8E3406Be1c188e144E960205EBE84. The rest are linked to numerous addresses of the cluster.

```

0xeb8c666fd0583986a70264e8417da060efc6a0bd
0x08c56fc2f230df3a6d4866ce256459aa8daeee37
0x323401a2053c7494fa569d71c2757bc95f371be2
0x74880c530bc43213b724fce037a54789b19eba36
0x59a1234d72d16b1279eac2d52ba13ce5ab01f341
0x986ea7bbbb42fa0f314eeec493eee1a42b68a8ca
0xb8f407ae47e867ba0de607a5aedfc854a60da03e
0x49917e9fdf5c46477ead5184687582df156251cb
0x3de4780276d6d3667fc57f03f7457d128012e900
0xd70d40b06dc869202216e4158e807333cf3a8d3c
0x6491b25c2bccb96d117eb1bdc5a67ce619a2c0df
0x2f10dd94850bb76ec929c4db8a0f43a9bdc91134
0x3f92d252103b0836b5a06673acbc14096249ed5b
0x59c7be2a9cb9f367033dd1c7d5531098b315b380
0xf0fa35fa9b1f0e443c901b2e127cd8c1d0285262
0x003851e5aca9167c1c0cfd09f73e64bb2768f631
0x5d35822e0ce560e874317e96af39e2e72db51ad1
0x5517d99568f5ce22ad6e445cc79bfc040b96778f
0x0c15c72c07b791acc5fd53d86de484c786738cbf
0xb6af5f2a8f05a1af50f180bf31e1ffa11bfe3ed6
0x5a4a61d54151c3e07e984aaa2716d33ba1808023
```

We can observe from the arkham modelization that the adresses are more than linked :

![image](https://github.com/99mitch/sybil-report/assets/163365834/9a4f336d-8957-4842-abe1-d1d613416800)

They have similar LZ Age (date of first L0 interaction), amount bridged, contract count, interacted source chains, Unique Active Days etc...

![image](https://github.com/99mitch/sybil-report/assets/163365834/9b4d2020-d4a7-42e1-88ca-2924e3c0613a)

Cluster + same CEX address + same adresses interactions pattern. This is surely a sybil cluster.

## CLUSTER 9

The first 10 addresses of the cluster share the same OKX deposit address 0xe0e4c1b6Eda8E3406Be1c188e144E960205EBE84. The rest are linked to numerous addresses of the cluster.

```

0xf67b969da936b4733bc75541ed3901ecedcaf353
0x4d4428b2d29080092842bca10edcf31b06d00c95
0x1411bccec4001c0eb18de07b1973caba9b7058e6
0x2f4c4a0080fb92bda321ff5cfd97d7f285a2f4ec
0x2c3517f6a15944d3adb960f0d1c5dd475b252bc2
0x8a6bf259bd79b03e069a32df22727b55570f8b35
0xc476fdbaa63682d23bf8fcda9e9de59affb9153e
0x153eea2d6a7cf03c2c229a19bccb8571182596f5
0x5abdc9108087fa8c8a3b2eab94a3daf23b30c012
0xc3e65dede3aee84e8877c1646e2cee5aa22068fa
0x8385452ba02a588dfe4753544995d688c7fdd1f5
0xca85ef9af5f64eea898eb78dcc11aec3597a7b41
0x66e8bd359d576c4703096679753b8754e45577b8
0x892676e69f4912ff6ccfcdf3026254715cf64080
0xfcb9d6d9bc04361e7a69efd29d7d93856a81753c
0x8857535a6f35ffb94a7d2b4432424e52defcce71
0x7c9842d9e619ce85392855467cac761e0ac9b103
0xc25d4e71c3e2313ac70d5daaf2a3ffb57711a19b
0x5eca494f77ea7cb7ff7e3656de7104f391eaf100
0xd0e9c403bc33b79644564a1c04c273dad2517370
```

We can observe from the arkham modelization that the adresses are more than linked :

![image](https://github.com/99mitch/sybil-report/assets/163365834/cc9d58a0-67d1-4ddb-bedf-5cba116f9871)

They have similar LZ Age (date of first L0 interaction), amount bridged, contract count, interacted source chains, Unique Active Days etc...





# CLUSTER 10

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

# CLUSTER 11

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

<details>

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

</details>
  
The cluster shares the same CEX deposit address and exhibits identical on-chain activity simultaneously, it is undoubtedly a sybil operation.


# CLUSTER 12

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


<details>
![image](https://github.com/foukara/report.md/assets/170763146/d7970f41-5be3-4579-b6f8-369ff7cca016)
![Capture d'écran 2024-05-27 125954](https://github.com/foukara/report.md/assets/170763146/0666397b-c3af-4750-abef-8d953bb87840)
![Capture d'écran 2024-05-27 125908](https://github.com/foukara/report.md/assets/170763146/ce318c66-bea0-4a21-995f-1f4ac37969e2)
![Capture d'écran 2024-05-27 130100](https://github.com/foukara/report.md/assets/170763146/4b5e85d1-4099-4210-b3e4-4d13a6fff485)
![Capture d'écran 2024-05-27 130036](https://github.com/foukara/report.md/assets/170763146/31ece054-f990-435f-a6e3-f4560ec1d303)
![Capture d'écran 2024-05-27 130014](https://github.com/foukara/report.md/assets/170763146/a4ca5a11-6520-4b29-b282-5e6c177f1f7f)

</details>
  
The addresses of the cluster share the same on-chain activity. For example, they all used the Linea bridge multiple times in the same day timespan to bridge ETH.


# CLUSTER 13

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


Addresses in the cluster show similar activity on the chain, indicating the sybil nature of the cluster. For example, they have similar deposits/withdrawals on Binance on the same day (equel gas charges around $0.45). To this we can add an L2 Transaction via zkSync for the same amount on the same day (approximately $20).

<details>

![image](https://github.com/foukara/report.md/assets/170763146/ed92b899-ef87-42d0-bd2f-fa9359c3d61f)
![image](https://github.com/foukara/report.md/assets/170763146/4b54474b-e7d7-4165-8c79-514ef36a38a7)
![image](https://github.com/foukara/report.md/assets/170763146/5869f6e4-ac5c-4c76-86f4-c8061e09c313)
![image](https://github.com/foukara/report.md/assets/170763146/e4b60bd1-660e-415b-9f19-97ac16825539)
![image](https://github.com/foukara/report.md/assets/170763146/68b23f8e-997a-4391-97f5-0ceae8191bd8)
![image](https://github.com/foukara/report.md/assets/170763146/5e6d32e8-64b0-4693-8322-e6ff478c8522)
![image](https://github.com/foukara/report.md/assets/170763146/84eb984e-c188-4645-9c13-2e518d47b1e5)
![image](https://github.com/foukara/report.md/assets/170763146/3f350ee7-14d1-44e2-835a-f3c7b0a40bda)
![image](https://github.com/foukara/report.md/assets/170763146/d9ed1bb5-23f5-4b42-9d27-12fcd16854b3)
![image](https://github.com/foukara/report.md/assets/170763146/b9aa428f-33e5-49ab-be45-940416cb28d4)
![image](https://github.com/foukara/report.md/assets/170763146/cfbb4f9a-3a29-4f12-9bbd-4ae6beee4f79)
![image](https://github.com/foukara/report.md/assets/170763146/3cce7ccb-3ab7-4ce2-8727-23f19d6facd8)
![image](https://github.com/foukara/report.md/assets/170763146/3bf14cd3-cbce-402c-a9a8-9043ce71b7fe)

</details>

Cluster + same CEX deposit address + same transactions are the same time in order to farm airdrop accross +20 wallets.

# CLUSTER 14

The first 27 addresses of the cluster share the same Binance deposit address 0x904f23f8E97adb1e706B2F1bcFc19ef47E32cE05. The rest are linked to numerous addresses of the cluster, multiple times.

```
0x0c55fe07ad75c135c797422a5857347b2e5a591e
0xe9ba7506dc9a35c1fa39cbdafdcb97436f855f50
0xc1889117a51e432a7f8ef454faf203f399bcff23
0xfefacd2ce98cdec5b072880d06c24af161b12727
0x1ba02368c020d5dbdfdf16fee1beec30dcf5d305
0x7313b87bc197b6c09f5928710dd80e2950535c27
0x741fa339367ce5da1f77fcb56384d8caac248f2c
0x09165d195d9f50c82aac439840cc6198d69003de
0x5315a1c257fd6266f9608f31ac9b6501c98c5750
0xb0b91fef5e4af34f727797079dcda5ccac817a4b
0xe8c8a5273f086e57238640582430cbf1f6b205d7
0x9023f1ed962416848bf844162903ef4624b27a4f
0x664aaf07e08b5330707a096a27e7b683a19096d5
0xe21314d9657ffc45264fcd394d1479d87f494f40
0xceac14c2f5f30ac130ceaec761ef270a47935deb
0x366686b8f26a7f93a2d0464a83697d60e2517023
0xed3ccd7509d84974c3b5f215b1dd01e14f939f8c
0xde91603429c54692d34dfc18d7661ad4254307c1
0x6131c4ccfd1545c66acafb2414a26191d20d3175
0xbe846d7f28a4febcdb520ba11732843dc5cc224e
0x4af081f8f5208b0d2e6fdcb44837b986fd24bee7
0xdf69a02f4abe2c19f1f1cbf683740d32a1535b42
0x11dd48ecd09c0ec6aeee5df6baf076401bb5c504
0x77104860ec646778df9ef186564ef5b6ea162ebe
0x2ef3bbab6500c624bdd84c42340a750e23dddcbb
0x7fb88de9cdc6c842787f1088b971717e08e9668a
0xb4a98d074faf4749427c2b5d74685c9aba24782c
0x7dbb218f08f8280d3ecce67130f763d4892c8c13
0x5f5f102914b677304a37cd50dca26b6fc476176a
0x78f84e69bff277112ca8ed131bd271eea51cfeff
0x5ffa6123552ef694bcce48dacf112c8e1f61faf4
0x34a4249d78c4955b1373fe1e72167c63db7dd504
0x9546df81ba5f23d98763d22044622f1c9d29369c
0x0490fbb2d3ba6de4c78630619330edb08758325c
0x81dcf2b67cfcdd2c14541afedec401c5d96bc75d
0xec70496a575f85de24d97edeaa5dfe0bb5a33f5e
0x33de79d1864ad40d8e5d0b829e426dbf67d31d63
0x6a51bc515ac61c9b039051d0166674ff05fdd331
0x3c9377384bc6d94a3b1de35c741b1843c9cf885c
```

![image](https://github.com/foukara/report.md/assets/170763146/f49db0de-2209-40f5-8279-3ee1c8b9a5a7)

Addresses in the cluster share the same activity on the chain. For example, in this script we can see similar movements on the blockchains in the same order and within the same timeframes: ETH, Arbitrum, Scroll, Eigen, Arbinova, zKSync, Base, Linea, Starknet

<details>

scroll
```
1 0x0c55fe07ad75c135c797422a5857347b2e5a591e 2023-11-19 
2 0xe9ba7506dc9a35c1fa39cbdafdcb97436f855f50 2023-11-19 
3 0xc1889117a51e432a7f8ef454faf203f399bcff23 2023-11-19 
4 0xfefacd2ce98cdec5b072880d06c24af161b12727 2023-11-19 
5 0x1ba02368c020d5dbdfdf16fee1beec30dcf5d305 2023-11-19 
6 0x7313b87bc197b6c09f5928710dd80e2950535c27 2023-11-19 
7 0x741fa339367ce5da1f77fcb56384d8caac248f2c 2023-11-19 
8 0x09165d195d9f50c82aac439840cc6198d69003de 2023-11-19 
9 0x5315a1c257fd6266f9608f31ac9b6501c98c5750 2023-11-19 
10 0xb0b91fef5e4af34f727797079dcda5ccac817a4b 2023-11-19 
11 0xe8c8a5273f086e57238640582430cbf1f6b205d7 2023-11-19 
12 0x9023f1ed962416848bf844162903ef4624b27a4f 2023-11-19 
13 0x664aaf07e08b5330707a096a27e7b683a19096d5 2024-03-22 2023-12-24 2023-11-20 
14 0xe21314d9657ffc45264fcd394d1479d87f494f40 2023-11-19 
15 0xceac14c2f5f30ac130ceaec761ef270a47935deb 2023-11-19 
16 0x366686b8f26a7f93a2d0464a83697d60e2517023 2023-11-19 
17 0xed3ccd7509d84974c3b5f215b1dd01e14f939f8c 2023-11-19 
18 0xde91603429c54692d34dfc18d7661ad4254307c1 2023-11-19 
19 0x6131c4ccfd1545c66acafb2414a26191d20d3175 2023-11-19 
20 0xbe846d7f28a4febcdb520ba11732843dc5cc224e 2023-11-19 
21 0x4af081f8f5208b0d2e6fdcb44837b986fd24bee7 2023-11-19 
22 0xdf69a02f4abe2c19f1f1cbf683740d32a1535b42 2023-11-19 
23 0x11dd48ecd09c0ec6aeee5df6baf076401bb5c504 2023-11-19 
24 0x77104860ec646778df9ef186564ef5b6ea162ebe 2023-11-19 
25 0x2ef3bbab6500c624bdd84c42340a750e23dddcbb 2023-11-19 
26 0x7fb88de9cdc6c842787f1088b971717e08e9668a 2024-03-28 2023-11-19 
27 0xb4a98d074faf4749427c2b5d74685c9aba24782c 2024-03-22 2023-12-24 2023-11-21 
28 0x7dbb218f08f8280d3ecce67130f763d4892c8c13 2023-11-19 
29 0x5f5f102914b677304a37cd50dca26b6fc476176a 2024-03-22 2023-11-19 
30 0x78f84e69bff277112ca8ed131bd271eea51cfeff 2024-03-28 2023-11-19 
31 0x5ffa6123552ef694bcce48dacf112c8e1f61faf4 2024-03-28 2023-11-19 
32 0x34a4249d78c4955b1373fe1e72167c63db7dd504 2024-03-28 2023-11-19 
33 0x9546df81ba5f23d98763d22044622f1c9d29369c 2024-03-22 2023-11-19 
34 0x0490fbb2d3ba6de4c78630619330edb08758325c 2024-03-28 2023-11-19 
35 0x81dcf2b67cfcdd2c14541afedec401c5d96bc75d 2024-03-22 2023-11-26 
36 0xec70496a575f85de24d97edeaa5dfe0bb5a33f5e 2024-03-22 2023-11-19 
37 0x33de79d1864ad40d8e5d0b829e426dbf67d31d63 2023-11-19 2023-11-19 
38 0x6a51bc515ac61c9b039051d0166674ff05fdd331 2023-11-19 
39 0x3c9377384bc6d94a3b1de35c741b1843c9cf885c 2024-03-22 2023-11-19 
```


arbinova
```
1 0x0c55fe07ad75c135c797422a5857347b2e5a591e 2023-02-26 2022-11-04 
2 0xe9ba7506dc9a35c1fa39cbdafdcb97436f855f50 2023-02-26 2022-11-04 
3 0xc1889117a51e432a7f8ef454faf203f399bcff23 2023-02-26 2022-11-12 
4 0xfefacd2ce98cdec5b072880d06c24af161b12727 2023-02-26 2022-11-12 
5 0x1ba02368c020d5dbdfdf16fee1beec30dcf5d305 2023-02-26 2022-11-12 
6 0x7313b87bc197b6c09f5928710dd80e2950535c27 2023-02-26 2022-11-12 
7 0x741fa339367ce5da1f77fcb56384d8caac248f2c 2023-02-26 2022-11-12 
8 0x09165d195d9f50c82aac439840cc6198d69003de 2023-02-26 2022-11-04 2022-11-03 
9 0x5315a1c257fd6266f9608f31ac9b6501c98c5750 2023-02-26 2022-11-04 
10 0xb0b91fef5e4af34f727797079dcda5ccac817a4b 2023-02-26 2022-11-04 
11 0xe8c8a5273f086e57238640582430cbf1f6b205d7 2023-02-26 2022-11-12 
12 0x9023f1ed962416848bf844162903ef4624b27a4f 2023-02-26 2023-02-25 2022-11-05 
13 0x664aaf07e08b5330707a096a27e7b683a19096d5 2023-02-26 
14 0xe21314d9657ffc45264fcd394d1479d87f494f40 2023-02-26 2022-11-04 
15 0xceac14c2f5f30ac130ceaec761ef270a47935deb 2023-02-26 2022-11-04 
16 0x366686b8f26a7f93a2d0464a83697d60e2517023 2023-02-26 2022-11-04 
17 0xed3ccd7509d84974c3b5f215b1dd01e14f939f8c 2023-02-26 2022-11-04 
18 0xde91603429c54692d34dfc18d7661ad4254307c1 2023-02-26 2022-11-04 
19 0x6131c4ccfd1545c66acafb2414a26191d20d3175 2023-02-26 2022-11-12 
20 0xbe846d7f28a4febcdb520ba11732843dc5cc224e 2023-02-26 2022-11-12 
21 0x4af081f8f5208b0d2e6fdcb44837b986fd24bee7 2023-02-26 2022-11-12 
22 0xdf69a02f4abe2c19f1f1cbf683740d32a1535b42 2023-02-26 2022-11-12 
23 0x11dd48ecd09c0ec6aeee5df6baf076401bb5c504 2023-02-26 2022-11-12 
24 0x77104860ec646778df9ef186564ef5b6ea162ebe 2023-02-26 2022-11-12 
25 0x2ef3bbab6500c624bdd84c42340a750e23dddcbb 2023-02-26 2022-11-12 
26 0x7fb88de9cdc6c842787f1088b971717e08e9668a 2023-02-26 2022-11-21 
27 0xb4a98d074faf4749427c2b5d74685c9aba24782c 2023-02-26 
28 0x7dbb218f08f8280d3ecce67130f763d4892c8c13 2023-02-26 2022-11-21 
29 0x5f5f102914b677304a37cd50dca26b6fc476176a 2023-02-26 2022-11-21 
30 0x78f84e69bff277112ca8ed131bd271eea51cfeff 2023-02-26 2022-11-21 
31 0x5ffa6123552ef694bcce48dacf112c8e1f61faf4 2023-02-26 2022-11-21 
32 0x34a4249d78c4955b1373fe1e72167c63db7dd504 2023-02-26 2022-11-21 
33 0x9546df81ba5f23d98763d22044622f1c9d29369c 2023-02-26 2022-11-21 
34 0x0490fbb2d3ba6de4c78630619330edb08758325c 2023-02-26 2022-11-21 
35 0x81dcf2b67cfcdd2c14541afedec401c5d96bc75d 2023-02-26 2022-11-21 
36 0xec70496a575f85de24d97edeaa5dfe0bb5a33f5e 2023-02-26 2022-11-21 
37 0x33de79d1864ad40d8e5d0b829e426dbf67d31d63 2023-02-26 2022-11-21 
38 0x6a51bc515ac61c9b039051d0166674ff05fdd331 2023-02-26 2022-11-21 
39 0x3c9377384bc6d94a3b1de35c741b1843c9cf885c 2023-02-26 2022-11-21 
```

zksync
```
1 0x0c55fe07ad75c135c797422a5857347b2e5a591e 2023-09-11 2023-07-30 
2 0xe9ba7506dc9a35c1fa39cbdafdcb97436f855f50 2023-11-16 2023-09-11 2023-07-30 
3 0xc1889117a51e432a7f8ef454faf203f399bcff23 2023-09-11 2023-07-30 
4 0xfefacd2ce98cdec5b072880d06c24af161b12727 2023-09-11 2023-07-30 
5 0x1ba02368c020d5dbdfdf16fee1beec30dcf5d305 2023-09-11 2023-07-30 
6 0x7313b87bc197b6c09f5928710dd80e2950535c27 2023-09-11 2023-07-30 
7 0x741fa339367ce5da1f77fcb56384d8caac248f2c 2023-09-11 2023-07-30 
8 0x09165d195d9f50c82aac439840cc6198d69003de 2024-04-24 2023-09-17 2023-09-11 2023-07-30 
9 0x5315a1c257fd6266f9608f31ac9b6501c98c5750 2024-04-24 2023-09-19 2023-09-19 2023-09-18 2023-09-11 2023-07-30 
10 0xb0b91fef5e4af34f727797079dcda5ccac817a4b 2024-04-24 2023-11-14 2023-11-14 2023-09-11 2023-07-30 
11 0xe8c8a5273f086e57238640582430cbf1f6b205d7 2023-09-11 2023-07-30 
12 0x9023f1ed962416848bf844162903ef4624b27a4f 2024-04-24 2023-09-17 2023-09-11 2023-07-30 
13 0x664aaf07e08b5330707a096a27e7b683a19096d5 2024-03-18 2024-02-04 2023-12-24 2023-11-24 2023-10-29 2023-10-02 2023-10-01 
14 0xe21314d9657ffc45264fcd394d1479d87f494f40 2023-09-20 2023-09-19 2023-09-19 2023-09-18 2023-09-11 2023-07-30 
15 0xceac14c2f5f30ac130ceaec761ef270a47935deb 2023-10-03 2023-09-11 2023-07-30 
16 0x366686b8f26a7f93a2d0464a83697d60e2517023 2023-09-11 2023-07-30 
17 0xed3ccd7509d84974c3b5f215b1dd01e14f939f8c 2023-10-11 2023-09-11 2023-07-30 
18 0xde91603429c54692d34dfc18d7661ad4254307c1 2023-11-12 2023-09-11 2023-07-30 
19 0x6131c4ccfd1545c66acafb2414a26191d20d3175 2023-09-11 2023-07-30 
20 0xbe846d7f28a4febcdb520ba11732843dc5cc224e 2023-09-11 2023-07-30 
21 0x4af081f8f5208b0d2e6fdcb44837b986fd24bee7 2023-09-11 2023-07-30 
22 0xdf69a02f4abe2c19f1f1cbf683740d32a1535b42 2023-09-11 2023-07-30 
23 0x11dd48ecd09c0ec6aeee5df6baf076401bb5c504 2023-09-11 2023-07-30 
24 0x77104860ec646778df9ef186564ef5b6ea162ebe 2023-09-11 2023-07-30 
25 0x2ef3bbab6500c624bdd84c42340a750e23dddcbb 2023-09-11 2023-07-30 
26 0x7fb88de9cdc6c842787f1088b971717e08e9668a 2024-03-18 2024-01-12 
27 0xb4a98d074faf4749427c2b5d74685c9aba24782c 2024-03-18 2024-02-04 2023-12-24 2023-11-19 2023-10-29 2023-10-03 2023-09-30 
28 0x7dbb218f08f8280d3ecce67130f763d4892c8c13 2024-03-18 2024-01-12 
29 0x5f5f102914b677304a37cd50dca26b6fc476176a 2024-03-18 2024-01-12 
30 0x78f84e69bff277112ca8ed131bd271eea51cfeff 2024-03-18 2024-01-12 
31 0x5ffa6123552ef694bcce48dacf112c8e1f61faf4 2024-03-18 2024-01-12 
32 0x34a4249d78c4955b1373fe1e72167c63db7dd504 2024-03-18 2024-01-12 
33 0x9546df81ba5f23d98763d22044622f1c9d29369c 2024-03-18 2024-01-12 
34 0x0490fbb2d3ba6de4c78630619330edb08758325c 2024-03-18 2024-01-12 
35 0x81dcf2b67cfcdd2c14541afedec401c5d96bc75d 2024-03-18 2024-01-12 
36 0xec70496a575f85de24d97edeaa5dfe0bb5a33f5e 2024-03-18 2024-01-12 
37 0x33de79d1864ad40d8e5d0b829e426dbf67d31d63 2024-03-19 2024-01-12 
39 0x3c9377384bc6d94a3b1de35c741b1843c9cf885c 2024-03-18 2024-01-12
```

</details>


Cluster + same cex deposit address + execute transactions at the same time with same amounts to farm airdrops.


# CLUSTER 15 

The first 25 addresses of the cluster share the same Binance deposit address 0xBF9D58b1c8d3E0495ab9097e71c433eB925B36e8. The rest are linked to numerous addresses of the cluster, multiple times.

```
0xc2f430299746e9ef8edf5bd72257f4082b1a2413
0x663bd9397e3769dcc3c0463baaba8d26335b6f85
0xb564260d051c5e9531341352962133c36f4ee198
0x101c632f6d6904a013688d0ef53374270835d11c
0x823f728e097d3168f9a26f580fc1d4ec3dae0bd8
0x8b42afc95c687dbf7c92f53add196bf247017d01
0x6f9db444db84a90fd01b3015d6e340a9c9cef6b9
0x74ccc4e0d7a99013a415d2b475c57aa24ac2c258
0x7fe1bc2edfe9848e8aeae84b256390d40a33f2ab
0x4f58b2de9d49de5dbc6c082b656af883be1c257d
0x9a44ce9b706f28dd52d3e500e65e030343be199d
0x7194b3f4607a4578a3f1d13e6ab634dce1910a73
0xc9bd1c3d353518d562c2de5d17857d94d1c63937
0xeaf1217d2deca7b0ac16f8ddd3aec1d28f7bca94
0x1e091e758a0b741c747679c239583f36f8ee6d31
0xce947c28b39d66e9d25c05f666c62f1cc03ec604
0x6aae079ec6a20b641938ba7fdf274f7c5bf4e5ae
0x2a4b99217b844dc9186847e7dfdc4924670bef05
0x7cf6e8194fb4a6a91bec444f285c65f98bddc790
0xbd33dc7c3364824b2ab4431bc4936073f532c533
0xd606d34d9bc25e34bcba3209dfca4ce5d545956e
0xe401569ae177751ba53f3da5fd32b5daa00eedfd
0x4050528925fbfffdc32ffa2ce8722ffbc621a1db
0xad09b90c9d49893c7a1378a7d9300e19ce2dc0ed
0x04620146fa7720ceff55bbc27e5aa08640652a45
0x52c97cf5beff5a3956e4d395e0a936baf87221c4
0xbada0b5ec9f4ab40040cd84f0859b1b19c7c0af7
```

![image](https://github.com/foukara/report.md/assets/170763146/11a49fa6-6134-4960-9fa7-0b626388498d)

The addresses have the same on-chain activity. They have similar LZ Age (date of first L0 interaction) many recurrences between 300/400/500 days, amount bridged, contract count, interacted source chains, Unique Active Days etc...

![image](https://github.com/foukara/report.md/assets/170763146/1f9e71a4-b1e5-45d0-bc25-388cddcff7b2)

We can quickly see in this script that the addresses share the same activity on the same date on zKSync, Arbinova and Scroll.

```
scroll
1 0x0c55fe07ad75c135c797422a5857347b2e5a591e 2023-11-19 
2 0xe9ba7506dc9a35c1fa39cbdafdcb97436f855f50 2023-11-19 
3 0xc1889117a51e432a7f8ef454faf203f399bcff23 2023-11-19 
4 0xfefacd2ce98cdec5b072880d06c24af161b12727 2023-11-19 
5 0x1ba02368c020d5dbdfdf16fee1beec30dcf5d305 2023-11-19 
6 0x7313b87bc197b6c09f5928710dd80e2950535c27 2023-11-19 
7 0x741fa339367ce5da1f77fcb56384d8caac248f2c 2023-11-19 
8 0x09165d195d9f50c82aac439840cc6198d69003de 2023-11-19 
9 0x5315a1c257fd6266f9608f31ac9b6501c98c5750 2023-11-19 
10 0xb0b91fef5e4af34f727797079dcda5ccac817a4b 2023-11-19 
11 0xe8c8a5273f086e57238640582430cbf1f6b205d7 2023-11-19 
12 0x9023f1ed962416848bf844162903ef4624b27a4f 2023-11-19 
14 0xe21314d9657ffc45264fcd394d1479d87f494f40 2023-11-19 
15 0xceac14c2f5f30ac130ceaec761ef270a47935deb 2023-11-19 
16 0x366686b8f26a7f93a2d0464a83697d60e2517023 2023-11-19 
17 0xed3ccd7509d84974c3b5f215b1dd01e14f939f8c 2023-11-19 
18 0xde91603429c54692d34dfc18d7661ad4254307c1 2023-11-19 
19 0x6131c4ccfd1545c66acafb2414a26191d20d3175 2023-11-19 
20 0xbe846d7f28a4febcdb520ba11732843dc5cc224e 2023-11-19 
21 0x4af081f8f5208b0d2e6fdcb44837b986fd24bee7 2023-11-19 
22 0xdf69a02f4abe2c19f1f1cbf683740d32a1535b42 2023-11-19 
23 0x11dd48ecd09c0ec6aeee5df6baf076401bb5c504 2023-11-19 
24 0x77104860ec646778df9ef186564ef5b6ea162ebe 2023-11-19 
25 0x2ef3bbab6500c624bdd84c42340a750e23dddcbb 2023-11-19 
28 0x7dbb218f08f8280d3ecce67130f763d4892c8c13 2023-11-19 
29 0x5f5f102914b677304a37cd50dca26b6fc476176a 2023-11-19 
30 0x78f84e69bff277112ca8ed131bd271eea51cfeff 2023-11-19 
31 0x5ffa6123552ef694bcce48dacf112c8e1f61faf4 2023-11-19 
32 0x34a4249d78c4955b1373fe1e72167c63db7dd504 2023-11-19 
33 0x9546df81ba5f23d98763d22044622f1c9d29369c 2023-11-19 
34 0x0490fbb2d3ba6de4c78630619330edb08758325c 2023-11-19 
36 0xec70496a575f85de24d97edeaa5dfe0bb5a33f5e 2023-11-19 
37 0x33de79d1864ad40d8e5d0b829e426dbf67d31d63 2023-11-19 
38 0x6a51bc515ac61c9b039051d0166674ff05fdd331 2023-11-19 
39 0x3c9377384bc6d94a3b1de35c741b1843c9cf885c 2023-11-19 

arbinova
1 0x0c55fe07ad75c135c797422a5857347b2e5a591e 2023-02-26 2022-11-04 
2 0xe9ba7506dc9a35c1fa39cbdafdcb97436f855f50 2023-02-26 2022-11-04 
3 0xc1889117a51e432a7f8ef454faf203f399bcff23 2023-02-26 2022-11-12 
4 0xfefacd2ce98cdec5b072880d06c24af161b12727 2023-02-26 2022-11-12 
5 0x1ba02368c020d5dbdfdf16fee1beec30dcf5d305 2023-02-26 2022-11-12 
6 0x7313b87bc197b6c09f5928710dd80e2950535c27 2023-02-26 2022-11-12 
7 0x741fa339367ce5da1f77fcb56384d8caac248f2c 2023-02-26 2022-11-12 
8 0x09165d195d9f50c82aac439840cc6198d69003de 2023-02-26 2022-11-04 2022-11-03 
9 0x5315a1c257fd6266f9608f31ac9b6501c98c5750 2023-02-26 2022-11-04 
10 0xb0b91fef5e4af34f727797079dcda5ccac817a4b 2023-02-26 2022-11-04 
11 0xe8c8a5273f086e57238640582430cbf1f6b205d7 2023-02-26 2022-11-12 
12 0x9023f1ed962416848bf844162903ef4624b27a4f 2023-02-26 2023-02-25 2022-11-05 
13 0x664aaf07e08b5330707a096a27e7b683a19096d5 2023-02-26 
14 0xe21314d9657ffc45264fcd394d1479d87f494f40 2023-02-26 2022-11-04 
15 0xceac14c2f5f30ac130ceaec761ef270a47935deb 2023-02-26 2022-11-04 
16 0x366686b8f26a7f93a2d0464a83697d60e2517023 2023-02-26 2022-11-04 
17 0xed3ccd7509d84974c3b5f215b1dd01e14f939f8c 2023-02-26 2022-11-04 
18 0xde91603429c54692d34dfc18d7661ad4254307c1 2023-02-26 2022-11-04 
19 0x6131c4ccfd1545c66acafb2414a26191d20d3175 2023-02-26 2022-11-12 
20 0xbe846d7f28a4febcdb520ba11732843dc5cc224e 2023-02-26 2022-11-12 
21 0x4af081f8f5208b0d2e6fdcb44837b986fd24bee7 2023-02-26 2022-11-12 
22 0xdf69a02f4abe2c19f1f1cbf683740d32a1535b42 2023-02-26 2022-11-12 
23 0x11dd48ecd09c0ec6aeee5df6baf076401bb5c504 2023-02-26 2022-11-12 
24 0x77104860ec646778df9ef186564ef5b6ea162ebe 2023-02-26 2022-11-12 
25 0x2ef3bbab6500c624bdd84c42340a750e23dddcbb 2023-02-26 2022-11-12 
26 0x7fb88de9cdc6c842787f1088b971717e08e9668a 2023-02-26 2022-11-21 
27 0xb4a98d074faf4749427c2b5d74685c9aba24782c 2023-02-26 
28 0x7dbb218f08f8280d3ecce67130f763d4892c8c13 2023-02-26 2022-11-21 
29 0x5f5f102914b677304a37cd50dca26b6fc476176a 2023-02-26 2022-11-21 
30 0x78f84e69bff277112ca8ed131bd271eea51cfeff 2023-02-26 2022-11-21 
31 0x5ffa6123552ef694bcce48dacf112c8e1f61faf4 2023-02-26 2022-11-21 
32 0x34a4249d78c4955b1373fe1e72167c63db7dd504 2023-02-26 2022-11-21 
33 0x9546df81ba5f23d98763d22044622f1c9d29369c 2023-02-26 2022-11-21 
34 0x0490fbb2d3ba6de4c78630619330edb08758325c 2023-02-26 2022-11-21 
35 0x81dcf2b67cfcdd2c14541afedec401c5d96bc75d 2023-02-26 2022-11-21 
36 0xec70496a575f85de24d97edeaa5dfe0bb5a33f5e 2023-02-26 2022-11-21 
37 0x33de79d1864ad40d8e5d0b829e426dbf67d31d63 2023-02-26 2022-11-21 
38 0x6a51bc515ac61c9b039051d0166674ff05fdd331 2023-02-26 2022-11-21 
39 0x3c9377384bc6d94a3b1de35c741b1843c9cf885c 2023-02-26 2022-11-21 

zksync
1 0x0c55fe07ad75c135c797422a5857347b2e5a591e 2023-09-11 2023-07-30 
2 0xe9ba7506dc9a35c1fa39cbdafdcb97436f855f50 2023-09-11 2023-07-30 
3 0xc1889117a51e432a7f8ef454faf203f399bcff23 2023-09-11 2023-07-30 
4 0xfefacd2ce98cdec5b072880d06c24af161b12727 2023-09-11 2023-07-30 
5 0x1ba02368c020d5dbdfdf16fee1beec30dcf5d305 2023-09-11 2023-07-30 
6 0x7313b87bc197b6c09f5928710dd80e2950535c27 2023-09-11 2023-07-30 
7 0x741fa339367ce5da1f77fcb56384d8caac248f2c 2023-09-11 2023-07-30 
8 0x09165d195d9f50c82aac439840cc6198d69003de 2023-09-11 2023-07-30 
9 0x5315a1c257fd6266f9608f31ac9b6501c98c5750 2023-09-11 2023-07-30 
10 0xb0b91fef5e4af34f727797079dcda5ccac817a4b 2023-09-11 2023-07-30 
11 0xe8c8a5273f086e57238640582430cbf1f6b205d7 2023-09-11 2023-07-30 
12 0x9023f1ed962416848bf844162903ef4624b27a4f 2023-09-11 2023-07-30 
14 0xe21314d9657ffc45264fcd394d1479d87f494f40 2023-09-11 2023-07-30 
15 0xceac14c2f5f30ac130ceaec761ef270a47935deb 2023-09-11 2023-07-30 
16 0x366686b8f26a7f93a2d0464a83697d60e2517023 2023-09-11 2023-07-30 
19 0x6131c4ccfd1545c66acafb2414a26191d20d3175 2023-09-11 2023-07-30 
20 0xbe846d7f28a4febcdb520ba11732843dc5cc224e 2023-09-11 2023-07-30 
21 0x4af081f8f5208b0d2e6fdcb44837b986fd24bee7 2023-09-11 2023-07-30 
22 0xdf69a02f4abe2c19f1f1cbf683740d32a1535b42 2023-09-11 2023-07-30 
23 0x11dd48ecd09c0ec6aeee5df6baf076401bb5c504 2023-09-11 2023-07-30 
24 0x77104860ec646778df9ef186564ef5b6ea162ebe 2023-09-11 2023-07-30 
25 0x2ef3bbab6500c624bdd84c42340a750e23dddcbb 2023-09-11 2023-07-30
```

Some examples in pictures below.

<details>

Scroll:

![image](https://github.com/foukara/report.md/assets/170763146/a85b2817-fa4c-4653-9157-73b63aa55efb)
![image](https://github.com/foukara/report.md/assets/170763146/0ad1972b-80d2-4b79-8bc7-bd97eaa87455)
![image](https://github.com/foukara/report.md/assets/170763146/7e917c53-3f2a-4512-addb-e15313412d97)
![image](https://github.com/foukara/report.md/assets/170763146/d0de856d-e46b-43be-8397-14a71ff66c97)

Arbinova:

![image](https://github.com/foukara/report.md/assets/170763146/05b854eb-d947-4c4f-bad3-485c73335936)
![image](https://github.com/foukara/report.md/assets/170763146/728d00bf-ec26-4832-b259-15f9dc070bcd)
![image](https://github.com/foukara/report.md/assets/170763146/fbed876d-4ea6-439e-a6b5-140b26d86ab6)
![image](https://github.com/foukara/report.md/assets/170763146/1000e8a5-e93b-482a-a3df-5bcf3c613856)

zKSync:

![image](https://github.com/foukara/report.md/assets/170763146/13803b57-1714-4fd3-8be3-3d03566d3b4f)
![image](https://github.com/foukara/report.md/assets/170763146/dd14f06d-ac33-4624-a324-ee9a6e39717e)
![image](https://github.com/foukara/report.md/assets/170763146/8a98bc12-6416-4b8b-b500-ef90f5aa8d7e)
![image](https://github.com/foukara/report.md/assets/170763146/26e912b5-f0fd-4072-b1c6-aee6f79fc789)

</details>

Considering the cluster that link all those addresses, the usage of the same CEX deposit address and the same on-chain activity, there is no doubt this is a cluster of Sybil nature.


# CLUSTER 16

The first 26 addresses of the cluster share the same OKX deposit address 0x0dE5F45Ea0a2013498680f7FEdae05294cF04560. The rest are linked to numerous addresses of the cluster, multiple times.

```
0x634463e09465b63ae5c14e87c930e27d81ee376d
0x76f9ad4ec3981097c3ffc06f8ec22f8fd4296dcb
0x839dae2c7ae0447aa4c95205020ae42873281b91
0x4d38b5d222b644b58f94c4c68fba416690b5e253
0xb54a146d12d87fee3dedc3b2ff1105d6aca13794
0xdfb630d2e6f20baafa9cfcbfd4c3038948dd5bca
0x32b1eb45132299e337f1368473e39c30eb390a0d
0x3df801034ebc63d1c975f3ab2e73e2eb212b8777
0xdd4dbf44b549ac327f797aa5e53c5c00e195332f
0xef69ea1c0e15540a5dce974f81cdf6ed360797ea
0x37a551832f73ad58d2703ad6095319a3f3f4dbc9
0x87df6291db161c4439bc5f9877ca9b47f70f46b3
0x6cfc3b24611d2263f9e01abc1bf5b1315907fbf4
0x1b59e268a9b06846a2d53ec5b73afc9de448af6d
0x48cda476cb5c2ab0c3a54fe1cfd254e768954345
0xca54ef8af852e7571f54da6793ce96c4fa3f722f
0x2631fc25e6fb0a21f2044a0ff2485dd426768ba5
0x6085e497069a8238fc14a6c6c770234e44994be4
0x6da1c784a01c227869cd22ba569cd20bcbbcdd0d
0x7e59a5ce59f0d56d9e794b3868598d7936890709
0x71990172b77380b947ec7b441642a22d083cdb33
0xd5a7b156a9bbc2613abdb9d6d5e9c61123849b1e
0xb07612ba565fb6d6306b2d55da493d9c824da4de
0x4ad5e406cee8810ed8fbbec5746a07aeffea88c4
0x60fd895590bf4e46ac5485107cc42357109c5438
0x520e877c78f8fbd5b0581e2dccd2a17f0acf2f76
0x4f294e5dea9d3b1139960a8ba766908ed19fbd33
```

![image](https://github.com/foukara/report.md/assets/170763146/50b7b2b2-f86a-40a2-b54d-bb1832058682)

The addresses have the same on-chain activity. For example, they all executed the same create lock and withdraw transaction <$58 from STG on Stargate on Arbitrum in the same time frame.

<details>


![image](https://github.com/foukara/report.md/assets/170763146/9e5c3184-3f39-46ab-ae6e-ab7055f86509)
![image](https://github.com/foukara/report.md/assets/170763146/4721b68e-62c1-4b60-a22e-7fb1a61840ab)
![image](https://github.com/foukara/report.md/assets/170763146/a8f833a5-8877-4702-bc16-b63a9302a33a)
![image](https://github.com/foukara/report.md/assets/170763146/b4e36511-3255-491e-856d-719408f70f61)
![image](https://github.com/foukara/report.md/assets/170763146/23c8ca9b-354c-41bf-a3ed-77def3a097c6)
![image](https://github.com/foukara/report.md/assets/170763146/725fdd6d-74aa-482c-9c44-806a202b79ad)
![image](https://github.com/foukara/report.md/assets/170763146/385dfb84-d76a-4d21-ac61-a226c2b3e16b)
![image](https://github.com/foukara/report.md/assets/170763146/ce4c14df-c1de-4132-acf3-17cc36a68f9d)
![image](https://github.com/foukara/report.md/assets/170763146/eac29ec5-11b9-4b92-a3d3-c1990f0ff111)
![image](https://github.com/foukara/report.md/assets/170763146/19ef0785-a1b1-4509-a093-d77ecc3038ca)
![image](https://github.com/foukara/report.md/assets/170763146/01a4f2a3-9708-484b-b3f3-9bc905ed4437)
![image](https://github.com/foukara/report.md/assets/170763146/3a2b0148-57a5-4d83-8d65-50864da0c2a7)
![image](https://github.com/foukara/report.md/assets/170763146/ab71622f-7fbb-4352-af05-525b7c16b203)
![image](https://github.com/foukara/report.md/assets/170763146/38d3e17c-6b98-4ead-8ac8-ff734f00352c)
![image](https://github.com/foukara/report.md/assets/170763146/ceec1229-5721-4ffa-bde9-44a342fdd051)
![image](https://github.com/foukara/report.md/assets/170763146/f2067d22-36c6-421f-a228-7e0288beb480)

</details>

This can go on and on with other examples. Cluster + same CEX deposit address + same on-chain activity.

# CLUSTER 17 

The first 9 addresses of the cluster share the same OKX deposit address 0x074c9ee2b8c088f7B90E6b6dA3e2d64a8040a62E. The rest are linked to numerous addresses of the cluster, multiple times.

```
0x8e160cb240e5e0d96c976c80b8d3e26bb64da8f3
0x5b2d5564339d44aa5ec6fa060a0edb16b6a1d34a
0xb031f0bd2c75ff7d5ffdeecf652996ff32463402
0xd0245f6a7c016772f7ab27d7353217bb4b762007
0xfceab24a690e34582515fa9a4f9998cb1c57f811
0x1bbaec282cd11e2983670820e4bcee629a23a2db
0x60bdaa123a0bd41364168d5dac87a8d12a08bf52
0xdd756af8e666900824a882aeb3370e82908c8762
0x66045c0428f5ec28f1f64367ca34bb5d4a8a7925
0xa7b1f2217daba342ed40e1df85ea735ccb30e7e3
0x7cb1063b461a62585cb9ffadca1266ee64ec7e8b
0xfc4019a383b1104e095bd57eb234edb38b3320b0
0x7d51caa26b146c3fb6891cdd48431e8cb1481c86
0x85257d75f1a1e3c6a30e6a0d3ec581133891cf02
0x4f6e26c4848333890e56f68f90f458ef906e9ca3
0x0c996f32206db8e245f795593a2ff498566c05ce
0x31361c89dd5683ee75c10df89b1704e9e6d00d72
0x8647fa2a8f321729775cf828ba63a6edc1abb179
0xea0811c6d288e66f06d046795c77663a7fe950ec
0x53ae6f4ac77fa803ca032948e85ef9136ad9cb9c
0x353f9d718a3485255c8e2eb53a138e0a61f0556c
0x8c28b345a319a1b0f9d93f562ed0917994e993b9
0x5cf6da9cf8640cf6ffea4b9a854c575dfb26fa23
```
The addresses have similar on-chain activity. They all have similar Age in days, transaction count and amount bridge.

![image](https://github.com/foukara/report.md/assets/170763146/ad07b319-751e-4638-b80e-51a72c05b16b)


Addresses execute a similar transaction originating from the same CEX address. Last but not least, have exactly the same activity, on same day, almst equal amount transaction. For example on Reactor Fusion with the redeem and mint functions found on each addy 

<details>

![image](https://github.com/foukara/report.md/assets/170763146/cb49e2c6-40e9-4f9f-bbd6-c687b47fe706)
![image](https://github.com/foukara/report.md/assets/170763146/4ad61cb8-db5f-4b39-b30e-b8c5ca55fb15)
![image](https://github.com/foukara/report.md/assets/170763146/00cec801-76e9-4f95-a6c6-f363b7adbfe8)
![image](https://github.com/foukara/report.md/assets/170763146/86158a40-2aee-4bdd-b806-0f6e7dd4f4c8)
![image](https://github.com/foukara/report.md/assets/170763146/5729b471-559b-4bee-a1df-d24f83c03444)
![image](https://github.com/foukara/report.md/assets/170763146/b819b295-a8bd-426d-b038-4a7c91b42a3e)
![image](https://github.com/foukara/report.md/assets/170763146/18cdb8bf-633a-4e22-bbe5-176701efa498)

</details>

Cluster + same CEX address + same activity accross +20 wallets to farm airdrop. This is without a doubt a sybil cluster.




![image](https://github.com/99mitch/sybil-report/assets/163365834/34b48860-437e-4d48-b21f-2887656a25b4)

Considering the cluster, the usage of the same CEX deposit address and the exact same on-chain behavior, there is no doubt this is an industrial scale sybil cluster managed with a script.

# CLUSTER 18
The addresses of the cluster share the same Binance deposit address 0x926e1F027351f3a216bA2789711aedE4544467B8. The rest are linked to numerous addresses of the cluster, multiple times.
```
0x220a6f204a8f8e6af9397c14ed019df08843ad3a
0x62bccddcf02f65bfc8b6a90e9678d9ba5689e174
0xabc67a49d7d75bd04fa1dae22cd4b8c4f796540a
0x7a4c8e3655d665f3e25ccd6b60b1b024629b3705
0x52b1e3ac180137a57231d0e562dd441c72d0f9e5
0x945057b10a2c1f4170178fa9d910241e4d17f546
0x75d25dfffff585b83b3f535b6ecad842fae3edd2
0xdc1ead8150beeeca0bc078881ccb4e1b4fd0abb6
0x0fe805304e49e993b2c59287000a2726330d2055
0xdaaa47da50c945bc97602cafe755cc2520ef2767
0x778023fdbde373f6dd13e39946412616ed119873
0x4e3e782053e560fdebd2be4a6c9a1f26c9a0faa4
0xbcccbf04cec0c7675955928bfa501f0535258c54
0xf3a82bc66f8b1397be2932c1cdc375153405a4a6
0x0539ea2214683632f51d0c995a204a1fd37f4b5a
0x3c320d49287e027967a1da048e901524de8f4666
0xd6e059dd8721083d766fab77efeb0191d89f6fcb
0xa4fafb2a712c8e7ff05128820ee1458495f9bfe8
0xc2e80d2715898d1dbedc729c0b69d589da7711c9
0x38da8174fe56b1efc6c9dd9ef4a03eabdc6e1596
0x88e62b22123754afc1f1095c8b939ba9fe0a941a
0x13dd1fb2e6bea092100876a6ff6fd31fa2e5aacf
0x9ab6ae3c3d080f613185e3aae8f1b7126ef4a43b
0xdca0f538d72b772d34a71eec383b135e5969f454
0x5878d75bf684e489ee6e7ea81213c68b56966154
0xa5762639ff1727c68b871dbac20d9bfb50e4615d
0xe4bea4d3e87299ada38bf6dc42fe9000eeceb6a6
0x6e06d26da609b8488ad20dfe3563047f7548246f
0x4e58bf6805d76b72447ccdc794db6d24316cf02c
0x3fd249d41d3f1444452329381aa07701cb754fcf
0x881f69aa89a41c69c7f44f07d9618c313e16ebc4
0xc0e459851ed330d6cba2ccd4f273fd8453bcf0a5
0x8aa3cbeef60630fec9f34642e29ee4aa1653b6da
0x25d45f33837122bbd9e70e46d072f1a0f8bb8d95
```
<img width="653" alt="Capture d’écran 2024-05-25 à 03 24 17" src="https://github.com/wardell11/sybil-report/assets/170775813/f2514301-8918-4360-9c95-d0b729273429">

The addresses all have the same on-chain activity. For example, their latest L0 interaction is exactly the same, the same dapps at the same time in the same order: Stargate, Orderly Network, Merkly.
<details>

<img width="1414" alt="Capture d’écran 2024-05-25 à 03 14 07" src="https://github.com/wardell11/sybil-report/assets/170775813/98799909-f674-4fc7-a5a0-896776d3351f">
<img width="1440" alt="Capture d’écran 2024-05-25 à 03 14 42" src="https://github.com/wardell11/sybil-report/assets/170775813/b549e9e3-9d94-4bd9-a5cb-0490cd09e7ca">
<img width="1440" alt="Capture d’écran 2024-05-25 à 03 15 08" src="https://github.com/wardell11/sybil-report/assets/170775813/9d51e9ac-8214-4995-86b8-ab31f3869a42">
<img width="1440" alt="Capture d’écran 2024-05-25 à 03 15 30" src="https://github.com/wardell11/sybil-report/assets/170775813/24e216f8-6116-4682-87a2-642ef408f90b">
<img width="1440" alt="Capture d’écran 2024-05-25 à 03 20 32" src="https://github.com/wardell11/sybil-report/assets/170775813/b28fe81b-3780-4411-9580-c53724dcedd2">
<img width="1440" alt="Capture d’écran 2024-05-25 à 03 20 53" src="https://github.com/wardell11/sybil-report/assets/170775813/3dddd3c5-7991-4c28-8b9e-baa7625c5713">
<img width="1440" alt="Capture d’écran 2024-05-25 à 03 21 15" src="https://github.com/wardell11/sybil-report/assets/170775813/7b12eec8-6bb2-4f54-b7bb-106533b66c0a">



</details>


The address share the same CEX deposit address, are part of a cluster with multiple links between one another, and have the same on-chain activity. This is a big scale sybil operation, probably the result of scripts.

# CLUSTER 19

The first 12 addresses of the cluster share the same Binance deposit address 0x9649E21c2e4E16A3C836adcdada8e26Cd8Cc197d. The rest are linked to numerous addresses of the cluster, multiple times.
```
0xb5e9a9ca597f4bec5bfe34b4739cc8b2820675bd
0xd608f0c48411225b43e0c7a13021ae72d806c6a8
0x2dfb59b81d0cb5b7c984bcc2e262dc9fbee74298
0xbc84340c6329316f310679a7e4d48a8a6b65192e
0xc6c4f5063f8f6424cac6bce801d9a25edcc4a426
0xdae1a193639e2f113bdfe26a2cbc6b6e0e415fb8
0x6776a0e5b5566a5c1be3e6edeeb6824da0448f21
0x00a75ba3ea17b3c2782f0756022d1452c43ba7ca
0xb90dccdcc5694938dbf2cbadd809448c74e5bcec
0x42eee9dddd3302a19816554fab88fc560acc0efa
0xd5d3a68d149783a6e4ed3c14e78a9f74b8e6ee6a
0xecd40ff016c263a06ebf6958854fecadb2622818
0x7a3e5a5640213898c5c657cae9b45f826c0b4896
0x7713b0258952da63990a6b80bf2237878a9d1092
0xcc4dd02e63d391e803aaa0cb01e454ff111eaef7
0xa040b8bed171622a53a6181cbe9c11529d323652
0x193605b78873b63c653c18d3aa1295efe1bcf97d
0x7862a8f01a06f74a3d3111bad8f12fa1fc26921d
0x8762fc4b59d71c6d06dcfbd856fe1b60bd4e7564
0x0baf5dc796e95157411e0e3eaa4b6dd1d4b41537
```
The addresses share the same on-chain activity. They execute the same transactions at the same time in order to farm airdrops across 20 wallets. For example, they all used Stargate to bridge and send the same amount of tokens ($100) to other cluster wallet addresses on the same day (many of them on June 25, 2023) and stopped using Layer 0 technology afterward.

<details>

0xb5e9a9ca597f4bec5bfe34b4739cc8b2820675bd
<img width="974" alt="Capture d’écran 2024-05-27 à 21 59 13" src="https://github.com/wardell11/sybil-report/assets/170775813/71261448-aad9-4a7d-9b68-4afd4e2cf217">

0x6776a0e5b5566a5c1be3e6edeeb6824da0448f21
<img width="1033" alt="Capture d’écran 2024-05-27 à 22 12 06" src="https://github.com/wardell11/sybil-report/assets/170775813/5fa1d40b-a20c-430c-abfe-56157804ca6f">

0x2dfb59b81d0cb5b7c984bcc2e262dc9fbee74298
<img width="969" alt="Capture d’écran 2024-05-27 à 22 13 28" src="https://github.com/wardell11/sybil-report/assets/170775813/00337592-8c0b-4d54-a5cb-f7f05fe2d68a">

0xb90dccdcc5694938dbf2cbadd809448c74e5bcec
<img width="977" alt="Capture d’écran 2024-05-27 à 22 14 58" src="https://github.com/wardell11/sybil-report/assets/170775813/ff3f365f-56a8-480e-a235-ac6f1eebd343">

0xd608f0c48411225b43e0c7a13021ae72d806c6a8
<img width="972" alt="Capture d’écran 2024-05-27 à 22 15 49" src="https://github.com/wardell11/sybil-report/assets/170775813/389ded77-5839-4e00-a40a-ab765cb10941">

0x00a75ba3ea17b3c2782f0756022d1452c43ba7ca
<img width="968" alt="Capture d’écran 2024-05-27 à 22 17 03" src="https://github.com/wardell11/sybil-report/assets/170775813/0a2f87f0-124c-412e-a4b7-e0151fff859f">

0x42eee9dddd3302a19816554fab88fc560acc0efa
<img width="974" alt="Capture d’écran 2024-05-27 à 22 17 59" src="https://github.com/wardell11/sybil-report/assets/170775813/2c0f17a2-4db2-46b5-81c1-813781854039">


</details>


Same activity for all addresses of the cluster.

Also, you can see on Dune that all addresses have the same number of transactions with the same amount and created 523 days ago.
<img width="956" alt="Capture d’écran 2024-05-27 à 22 20 13" src="https://github.com/wardell11/sybil-report/assets/170775813/fe0a514e-b481-42f6-ab5e-0177258b702e">

Same CEX deposit addresses, cluster, and exact same pattern of interaction with L0 with same amount to farm the airdrop. This is a clear sybil cluster.

# CLUSTER 20
The first 12 addresses of the cluster share the same Binance deposit address 0x6ff197905601F6b8F59e3F71849e6a060D1dfd97. The rest are linked to numerous addresses of the cluster, multiple times.
```
0x1ded3c31ec30a1c651c7d1eca0f7db3ad76d15ef
0x1da5407a15e082e5f538e1c9f1bf3dcf812d1e15
0x6798a4be28e12b6346466f60f7e94c9becbf8fe2
0x8bea8c2f05917b493e1d1747cafff272f9545ea5
0x5b84cfb2660d510674a8b6ccd01659d2521fd5c1
0x925c8c407f1a3d988a06a45015256e49831a081b
0x8afe0a71682ece04af3b64e425c9e01f6712a6c4
0xd5565d3a05b2290e4f4cb9e2cc0e272f1a888b67
0xa8d66237c06b495e6597b4cb7cffc822b391ea2c
0x3450a682e5afba4e05d796584bc6cad9d3eeb99c
0xe2f51aac758d19b34877f44af1b8f998e1e265b1
0x9b02750d4c5348afbc52d83c3c3be8fc427fb879
0x25b3bcc2d83567561d1813bd4a3703bed5832254
0x0e030bad7f9e779ffc53d45c0748d6741ca567ad
0xeb6112a29cd11918885dddbd7f3db7404642ea38
0x9f41bff8678ad97ff99642e60aca011bbb88f60f
0x2ac2c30912bc44756411a6ab971f073d139819a9
0x9f38c4436a29e77e0a57cda343664f13d1c0fdf7
0xd1300820518f362180c747cbeeeb11e443bb8cdf
0x7a32c64265209562c004c8298e7ee0edcff07c83
```
<img width="605" alt="Capture d’écran 2024-05-27 à 23 41 46" src="https://github.com/wardell11/sybil-report/assets/170775813/da7ddd8e-39b0-4bf0-81b9-91a9fc460a5a">

The addresses have the same on-chain activity. For example, their L0 interaction follow the same pattern. They interact with the same dapps in the same order in the same timespans. 
As you can see : deposit 100$ + add liquidity 100$ on Stargate with all cluster addresses. 

<details>

0x8bea8c2f05917b493e1d1747cafff272f9545ea5
<img width="979" alt="Capture d’écran 2024-05-27 à 23 55 34" src="https://github.com/wardell11/sybil-report/assets/170775813/dbfb21cb-1fc0-4216-9d07-01a30471cc6b">

0x925c8c407f1a3d988a06a45015256e49831a081b
<img width="960" alt="Capture d’écran 2024-05-28 à 00 01 22" src="https://github.com/wardell11/sybil-report/assets/170775813/dae4330d-c0fe-4378-b252-e2edeb05b692">

0xa8d66237c06b495e6597b4cb7cffc822b391ea2c
<img width="971" alt="Capture d’écran 2024-05-28 à 00 02 47" src="https://github.com/wardell11/sybil-report/assets/170775813/e0760655-5bdc-473d-b26c-87750c4ebd24">

0x1da5407a15e082e5f538e1c9f1bf3dcf812d1e15
<img width="966" alt="Capture d’écran 2024-05-28 à 00 03 53" src="https://github.com/wardell11/sybil-report/assets/170775813/4efaf535-757c-4030-abc6-afb1c5040641">

0x1ded3c31ec30a1c651c7d1eca0f7db3ad76d15ef
<img width="957" alt="Capture d’écran 2024-05-28 à 00 04 55" src="https://github.com/wardell11/sybil-report/assets/170775813/050a0f17-02fa-48c5-933a-d7859ca250a0">

0x5b84cfb2660d510674a8b6ccd01659d2521fd5c1
<img width="964" alt="Capture d’écran 2024-05-28 à 00 06 47" src="https://github.com/wardell11/sybil-report/assets/170775813/e40d667d-bade-443c-af97-6bc4732710c6">




</details>


 We can see on Dune than all addresse have around 40-50 transactions with the same total amount of 18.000$ and created 610 ago.
<img width="958" alt="Capture d’écran 2024-05-28 à 00 26 17" src="https://github.com/wardell11/sybil-report/assets/170775813/76064f73-fb5c-43ab-99ba-1a2e25bb7cbb">

In conclusion, Same CEX deposit addresses, cluster, and exact same pattern of interaction with L0 with same amount to farm the airdrop(100$ deposit + Add liq on stargate with all addresses). This is a clear sybil cluster.
