# Isolated Lending

## Liquidation&#x20;

To participate in liquidations you can:

1. Directly interact with the IsolatedLendingV01 contract (see contract list) and call liquidate()
2. Create your own scripts / bot to liquidate

{% hint style="info" %}
nenofi IsolatedLendingV01 allows to liquidate 100% of borrowers debt whenever their borrow amount is greater than the pool's liquidation threshold or `CLOSED_COLLATERAZATION_RATE`
{% endhint %}

### Prerequisite

To execute a liquidation call, you need to know:

* The user address/account that borrows within a particular isolated lending pool
* The user's solvency
  * By calling `isSolvent(address user_address)`
  * Solvency is determined by `userCollateralValue(address user_address) * CLOSED_COLLATERAZATION_RATE >= totalAmountBorrowed(address user_address)`
  * `CLOSED_COLLATERAZATION_RATE` are different for each pool (see: pools)
* The user's amount of debt&#x20;
  * By calling`totalAmountBorrowed(address user_address)` you can get the borrowed amount.

### Liquidating a User

* If `isSolvent(address user_address)` returns false than that user is able to be liquidated.
  * Liquidation bonus are different for each pool (see: pools)
* Check user's borrowed amount by calling `totalAmountBorrowed(address user_address)`
  * nenofi IsolatedLendingV01 allows liquidator to liquidate 100% of borrowed amount
* Call `liquidate(address user_address, uint256 amount)` to liquidate insolvent users.\




