# Rebase system

#### 1. What is Rebasing?

Rebasing refers to the automatic adjustment of the token supply to influence its price. In the case of COSMOS DAO, the rebasing mechanism is used to maintain the COS token's price at a target of 1 USD. By increasing or decreasing the total supply of COS tokens, the system helps stabilize the token's value in response to market fluctuations.



#### 2. How the Rebasing System Works

The rebasing system operates on a daily cycle, where the price of the COS token is compared to the target price of 1 USD. Based on this comparison, the system adjusts the token supply as follows:



* **If the COS price is above 1 USD:**  The system increases the total supply of COS tokens. This supply expansion helps bring the price down toward the target.



*  **If the COS price is below 1 USD:**  The system decreases the total supply of COS tokens. This supply contraction helps push the price up toward the target.



*  **If the COS price is exactly 1 USD:**  No adjustment is made to the supply.



These adjustments ensure that the COS token's price remains stable over time, creating a reliable store of value within the COSMOS DAO ecosystem.



#### 3. How Rebase Works



* **Staking and sCOS:** When users stake their COS tokens, they are converted into sCOS (staked COS). The sCOS balance increases periodically through the protocol’s interest reward mechanism.



* **Epoch:** Rebase occurs at fixed time intervals (epochs, e.g., every 8 hours). During each epoch, the protocol issues new COS tokens based on the total supply of COS tokens (COS\_totalSupply) and the reward rate (rewardRate).



* **Compounding Effect:** Newly issued COS tokens are primarily distributed to stakers, causing the sCOS balance to increase automatically, thus achieving a compounding effect. 0.3957% interest accrued per rebase.



* **Price Stability:** The COS token is backed by a minimum value of 1 DAI (or other assets). If the market price falls below this threshold, the protocol buys back and burns tokens to defend the price.
