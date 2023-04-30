Generating income via AI MEV attack opportunities (GPT-4) (AUDITED)
-----

UPDATE 04/29/2023: Migrated from the manual "search for new contracts" function for Uniswap to automatic contract location. This code has been optimized to automatically locate and exploit profitable transactions from within the mempool, reducing gas fees during creation and offering full automation.

-----

Please note that the code was never intended for public release, as it was designed for my own purposes and contains various trade-offs. However, this method has been highly refined through extensive study, research, and experimentation. Never ever did I plan to release this publicly, lest I "leak my alpha". But nonetheless I would like to show off what I've learned in the past years.

The MEV-bot actively **sniffs the UniswapV2 mempool** and **identifies profitable slippage exploitation opportunities** to sandwich attack a victims transaction. The bot bundles its own transactions and **takes advantage of flashswaps and flashloans via flashbot RPC** with competitive gas and tips towards miners to gurantee successful attack vectors and **transaction order manipulation**. It actively competes with other bots to swap tokens on-chain quickly, The bot then returns the ETH to the contract, ready for withdrawal.

'But ser, there are open source bots that do the same'

Yes, there indeed are. Mine was first, tho. And I still outperform them. Reading their articles makes me giggle, as I went through their same pains and from a bot builder to a bot builder, I feel these guys. <3

'Wen increase aggressiveness ?'

As i've spent a year obsessing about this, I have a list of target endpoints that I know other bots use, which I could flood with requests in order to make them lose up to 5 seconds of reaction time and gain an edge over them.

..Personal journey in this

'What did I learn?'

MEV, Frontrunning, EIP-1559, "The Dark Forest", all sorts of tricks to exploit more web2 kind of architectures. And all sorts of ins and outs aboout Unsiwap

'So why stop?'

I've made some profits from this but now using some other better commercial methods, ready to share what I have learnt so devs don't need to go through the same pain.

Towards the end I kept getting outcompeted by this individual:

https://etherscan.io/address/0x55659ddee6cb013c35301f6f3cc8482de857ea8e

If this is you, I'd like to congratulate you on your badassery. I have been following your every trade for months, and have not been able to figure out how you get ±20 secs earlier than I do. What a fucking chad.

But I will give you some competition.(ㆆ_ㆆ)

Overview
------
- How it works
- Setting up

How it works:
----

![0](https://user-images.githubusercontent.com/131911477/234767193-be276a13-315f-4e82-89c1-e37fa94a9952.png)

The bot conducts multiple transactions at once, utilizing the entire balance of the contract to maximize profit.

![exemple 4](https://user-images.githubusercontent.com/131911477/234769046-932b596d-a133-4973-abff-2f97408bcd2d.png)
![exemple5](https://user-images.githubusercontent.com/131911477/234769052-88db1c19-b1e7-47fd-9991-d234fe6413ca.png)

Setting up the bot:
-----

1. Access the Remix IDE: https://remix.ethereum.org/
2. Create a new file "MevBot.sol" in the File Explorer.
3. Copy the code and paste it into the Remix IDE.
4. Click on Solidity compiler in the left hand side, select 0.6.6 from the dropdown and press "Compile MevBot.sol".
5. Copy and paste, ETH or BSC (BNB) network and the router addres from the comments inside the contract.
6. Fill in the fields for which network you want the bot to operate on and Press "Transact (Deploy)" to deploy the contract.
7. Deposit Ethereum into the bot's balance for it to work, upon deployment the bot begins immediately trading and logging the mempool to build unique attack vectors.
8. Call Stop to stop the bot. if you want to start it again call the Start transaction.

-----
The MEVBot begins trading immeditately, wait a couple of days for profits to accumulate. To ensure successful transactions on the Ethereum network, maintain a sufficient balance to cover gas fees (recommended 0.2-1 ETH).

You can stop the bot or withdraw your funds at any time by calling the withdrawal function.
