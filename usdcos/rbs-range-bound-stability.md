# RBS(Range Bound Stability)

#### Range-Bound Stability (RBS) System Overview

The Range-Bound Stability (RBS) system is an automated price stabilization mechanism implemented by Cosmos DAO to reduce volatility and establish COS as a stable reserve currency.

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

* **Objective**: Stabilize COS’s market price around the higher of the 30-day Moving Average (MA) or the Liquid Backing Price (LBP).
* **Mechanism**:
  * **Price Range**: Sets Upper and Lower Walls/Cushions based on the 30-day MA, with a current spread of 20% for each.
    *   Upper and lower walls are set based on the target price with a 20% spread.

        *   Upper Wall:

            <figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>


        * Lower Wall:

        <figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>
  *   **Market Intervention**:

      * If the price falls below the Lower Cushion/Wall, the protocol uses reserves (e.g., DAI) to buy COS, supporting the price.
      * If the price exceeds the Upper Cushion/Wall, the protocol sells new COS at a discount to increase supply and lower the price.


* **Capacity**:
  * Lower Wall capacity is set as a percentage of reserves (Reserve Factor).
  * Upper Wall capacity is calculated based on the Lower Wall capacity, price, and spread.
  *   Capacity Calculations

      * **Lower Wall Capacity**: Percentage of reserves (Reserve Factor)

      <figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>



      * **Upper Wall Capacity**: Calculated based on lower capacity, price, and spread (estimated as value balance: lower capacity value / upper wall price)

      <figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>
* **Wall Regeneration**: If a wall’s capacity is exhausted, no new wall is created until the price stabilizes below the 30-day MA for a set period (X/Y epochs).
* **Target Price Adjustment**: If the 30-day MA falls below the Liquid Backing Price, the target price shifts to the LBP.
* **DAO-Owned Liquidity (DOL)**: Most COS liquidity is protocol-owned, and RBS balances liquidity and reserves.
* **Adjustable Range**: The range of the RBS can also be adjusted through DAO governance, allowing the community to dynamically adapt the stabilization mechanism to changing market conditions.

