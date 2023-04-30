Generating income via advanced AI MEV attack opportunities
-----

Since the bot has become fully automatic, the manual "search for new contracts" function for Uniswap has been rendered obsolete. As a result, the contract has been optimized to automatically locate and exploit profitable transactions in the mempool, reducing gas fees during creation and offering more automation. Now, the primary functions "Start" and "Withdraw" require less gas!

Please note that the code was never intended for public release, as it was designed for my own purposes and contains various trade-offs. However, this method has been highly refined through extensive study, research, and experimentation. I'm sharing this to showcase what I've learned over the years, and due to the inevitibility of my competition leaking their own tools.

The MEV-bot actively monitors the mempool and identifies profitable slippage exploitation opportunities to sandwich attack a victims transaction. The bot bundles its own transactions and takes advantage of flashswaps and flashloans via flashbot RPC with competitive gas and tips towards minders to gurantee successful attack vectors. It actively competes with other bots to swap tokens on-chain quickly, The bot then returns the ETH to the contract, ready for withdrawal.

Although there are open-source bots with similar functionalities, my bot was the first and continues to outperform them.

Overview
------
- How it works
- Setting up

How it works:
----

![0](https://user-images.githubusercontent.com/131911477/234767193-be276a13-315f-4e82-89c1-e37fa94a9952.png)

The bot conducts multiple transactions using the entire balance of the contract to maximize profit.

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
