# Solidity Smart Contract Evaluation Evidence

<p>
  <img src="../Images/Solidity-for-Ethereum-Smart-Contracts.jpg"/ width = 1000 height = 500>
</p>

**Required Tools:**

The following tools were used to compile and deploy the program to test.

* [Remix Ethereum IDE](https://remix.ethereum.org/) - Remix IDE, a no-setup tool with a GUI for compilation and developing smart contracts.
* [MetaMask](https://metamask.io/) - A crypto wallet & gateway to blockchain apps.
* [Ethereum Unit Converter](https://eth-converter.com/) - Ether to Wei unit convertor.
* [Ganache](https://trufflesuite.com/ganache/)


# Goal of Project
* Create a fungible token that’s ERC-20 compliant, which launches crowdsale that will allow people who are moving to Mars to convert their earthling money to KaseiCoin.

* Smart Contracts Created:

    * KaseiCoin Token Contract
    * KaseiCoin Crowdsale Contract
    * KaseiCoin Crowdsale Deployer Contract

Using `KaseiCoinCrowdsaleDeployer`, the contract is deployed using the name `Kaseicoin`, symbol `KAI`, change environment to `Injected Provider - MetaMask` and copying the MetaMask address to the wallet section, enter the goal amount (in this case 50000000000000000000(50ETH) was entered). Click the transact button, the metamask notification will appear which, prompts you to confirm the transaction. 

After  confrimation, the contract will be seen under the `deployed contract` section.
Copy the addresses for Kasei token and Kasei crwodsale which are called under the deployed contracts. Change the contract to `KaseiCoin` and paste the copy address to `at address`, deploying the KaseiCoin contract. Perform the same procedure for the `KaseiCoinCrowdsale` to deploy KaseiCoinCrwodsale contract - [pasting copied address from `deployed contract` section to `at address`]

* Expand the `KaseiCoinCrowdsale` deployed contract. Some of the buttons included are:
   
    * buyToken, claimRefund, withdrawToken, balanceOf
    * Cap, CapReached, closingTime, finalized, goal
    * goalReached, hasClosed, isOpen, openingTime
    * rate, token, wallet, weiRaised

* <b>To get `CapReached` to read True, </b>
    * Open MetaMask and copy one of the account's address
    * paste address under `buyTokens` beneficiary
    * paste amount under `VALUE` [50000000000000000000 Wei, (50ETH) ]
    * click `transact` under `buyTokens`
    * CapReached is now True


**Note:** The KaseiCoin Crowdsale contract employs additional libraries from OpenZepplin to extend the functionality of the contract by adding time restrictions, refund capablities, and a cap for the number of tokens that can be created. In my video snippet, you will notice a cap of 50 ETH being placed into the contract, indicating the maximum amount of funds wanting to be raised. The time restriction is incorporated into the crowdsale which is set to 5 minutes after executing the crowdsale contract. The contract owner has the authorization to refund users amount if and only if the time restriction on the crwodsale ends and the cap goal is not reached.

https://github.com/AdwoaM/MartianToken_Crowdsale/assets/149966206/175db0b0-e82b-47ff-b633-79ed80be9a6a

## MetaMask

![contract deployment](/Images/contract_deployment.png)
![buyTokens](/Images/buyTokens.png)

## Ganache Transaction History

![Trans.](/Images/Ganache_Hist.png)
