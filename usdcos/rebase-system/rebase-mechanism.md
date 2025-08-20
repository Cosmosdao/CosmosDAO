# Rebase Mechanism

#### 1. Key Variables

The following variables are used in the COSMOS DAO rebase mechanism:

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure></div>

#### **2. 30-Day Moving Average Price**

The 30-day moving average priceMA30 is calculated as the average of the daily closing prices of the $COS token over the past 30 days:

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure></div>



#### **3. Rebase Conditions**

The rebase mechanism triggers when the market pricePt deviates by more than ±20% from the 30-day moving averageMA30.&#x20;

The conditions are:

*   **Price exceeds MA30 by more than 20%:**

    <div data-full-width="true"><figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure></div>

    &#x20;                                                          Increase the supply to lower the price.
* **Price falls below MA30 by more than 20%:**

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

<p align="center">  Decrease the supply (via buybacks and burns) to raise the price.</p>

*   **Price within ±20% ofMA30:**

    <figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

<p align="center">        No supply adjustment.</p>

<p align="center"></p>

#### **4. Supply Adjustment**

he supply adjustment during a rebase is calculated based on the deviation of the market pricePt from MA30. The goal is to bring PricePt closer to MA30:

*   **Supply increase (when price is too high):**

    <div align="left"><figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure></div>
* **Supply decrease (when price is too low):**

<div align="left"><figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure></div>

* **New supply:**

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>



#### **5. Staking Rewards and Compounding**

Staked $COS tokens (xCOS) accrue an interest rate ( r ) per rebase, which is determined by DAO governance (e.g., the current example rate is 0.3957%).&#x20;

The xCOS balance is updated as follows:

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

With three rebases per day (every 8 hours), the daily compounding effect is:

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

The annual compounding effect (365 days, approximately 1095 rebases) is:

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

**Note**: The interest rate ( r ) is not fixed and is subject to change based on DAO governance decisions. The current rate of 0.3957% is provided as an example.



#### 6. Price Defense Mechanism

If the market pricePt falls below the minimum backing valueBt = DAI, the protocol initiates buybacks and burns using Treasury assets.&#x20;

The buyback amount is:

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

The supply after burning is:

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

The Treasury’s asset value decreases after the buyback:

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

#### 7. Treasury Backing Constraint

Each $COS token must be backed by at least 1 DAI, ensuring the Treasury’s asset value satisfies:

<figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

