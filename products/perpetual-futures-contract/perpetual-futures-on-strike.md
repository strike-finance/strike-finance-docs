# Perpetual Futures  On Strike

Perpetual futures on Strike Finance have a few differences from traditional perpetual futures. There is no perpetual contract price; instead, there are entry prices.

The main benefits of perpetual contracts are still present:

1. Users can hold a position indefinitely, earning periodic payments if the market moves in their favor.
2. Traders can use leverage to earn multiples of their current capital.

### Funding Periods

Funding rounds occur at 8-hour intervals to determine profits for traders. At the start of each round, an oracle provides the asset's current price. After 8 hours, the asset's price is recorded again. The price movement during this interval determines which side profits:

* If the price increases between the start of the funding round and 8 hours later, the long side gains.
* If the price decreases between the start of the funding round and 8 hours later, the short side gains.

The profit is calculated based on the percentage difference between the entry and exit prices. The losing side pays this percentage to the winning side. Individual traders on the winning side receive a portion of the total profit, proportional to their share of the total asset amount on that side. For example, if a trader holds 10% of the total long position and the long side wins, they would receive 10% of the total profit distributed to longs.

### Margin Requirements

Strike Finance allows users to leverage their positions with an initial margin requirement of 25% and a minimum maintenance margin of 15%. For example, a trader with 100 ADA as collateral can borrow up to 300 ADA, creating a total position of 400 ADA. At the outset, the trader's equity (the difference between the position value and the loan) is 100 ADA, which meets the initial 25% margin requirement.

A trader's equity is calculated as follows:&#x20;

**Equity = Current Value of Assets − Loan Amount**

If after the funding round ends, the total value of the position drops 20% to 320 ADA, the new equity would be 20 ADA.

**20ADA = 320 ADA - 300 ADA**&#x20;

A minimum of 15% equity is required to maintain the position, which in this case is 48 ADA. Since the current equity (20 ADA) is below this threshold, the trader's position will be liquidated. This scenario demonstrates how market movements can quickly affect a leveraged position, potentially leading to liquidation if the equity falls below the minimum requirement.
