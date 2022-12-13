# Isolated Lending

## Overview

Most lending protocols allow users to deposit assets as collateral and borrow other assets against said collateral while pooling all of the assets all together. This is a major limitation and huge potential risk. It is a huge risk because if there's just one bad asset in the pool, it will effect the whole pool making the whole ecosystem accumulates bad debt. Thus, most lending protocols are very careful on adding new assets to their ecosystem making it a limitation and inaccessible for assets that are not listed.

We solve these issues by having a platform with:

* Isolated lending pairs. Anyone can create a pair, our team will help to create those pairs to onboard new assets to Lend/Borrow.
* Our team will curate the pairs, and it’s up to users which pairs they find safe enough. Risk is isolated to just that pair.
* Pool's oracle is up to the one who created the pool.
* Dynamic and Liquid interest rate.
* Optimized contract for low gas.

### Isolated Lending Pairs[​](https://docs.sushi.com/docs/Developers/Kashi%20Lending/Overview#isolated-lending-pairs) <a href="#isolated-lending-pairs" id="isolated-lending-pairs"></a>

Notable protocols such as Compound and Aave and, allow users to supply a variety of collateral assets and borrow another set of assets. However, if there is one bad asset within the system and that asset price drops rapidly before liquidators and liquidate, every single user will be affected by this. The platform's risk is therefore determined by the risk level of the riskiest asset on it. Adding more assets increases this risk, leading to a limited number of assets available on most platforms. Protocols such as Scream and Rari Capital lost tons of users' fund because of this.

With NenoFi isolating lending pairs, anyone can create a new pair and our team will help you set up a pair for your asset if needed. Some lending pairs will be very stable and safe, others not so much if they include highly volatile assets, low liquidity, and oracle failure. Because these are isolated pools, risk is limited to individual pools and interest rates will reflect that risk. Higher risk pools will attract less suppliers, hence pushing up the interest rate. We will curate the pool so that users will know which pool are riskier than others.

### Shorting or Longing Any Assets[​](https://docs.sushi.com/docs/Developers/Kashi%20Lending/Overview#margin-shorting-any-token) <a href="#margin-shorting-any-token" id="margin-shorting-any-token"></a>

NenoFi isolated pool will allow for the creation of thousands of lending pairs for any asset, creating the ability to go short/long on a large variety of assets. This is something that is in high demand, but currently not available for most assets.

Currently, there are some markets in which long/short position is prohibited.&#x20;

Let’s say we want to short GOTO

We supply $1000 worth of GOTO and borrow $700 worth of GOTO. We sell the GOTO for USDC and supply the USDC back to the pool. Now we have:

_Supply:_ $1700 USDC and Borrows: $700 GOTO

We borrow an extra $500 GOTO and sell it for USDC. We resupply the USDC and have:

_Supply:_ $2200 USDC and Borrows: $1200 GOTO

We can repeat this process a few more times. Depending on the collateral rate we can leverage 2–4x or more depending on our risk profile.

Now we are not only able to short this asset (which currently is often not possible, due to regulations or non existing market) but we can also leverage the short.&#x20;

### Revenue Generation[​](https://docs.sushi.com/docs/Developers/Kashi%20Lending/Overview#revenue-generation) <a href="#revenue-generation" id="revenue-generation"></a>

* 18% of the interest proceeds will be sent to NenoFi
* 2% of the interest proceeds will be to offset carbon
* 80% of the interest proceeds are for the lenders

