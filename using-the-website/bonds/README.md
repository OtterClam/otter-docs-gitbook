# Purchase A Bond \(1, 1\)

Bonds allow users to buy CLAM from the protocol at a discount by trading it with i\) liquidity \(LP tokens\) or ii\) other assets. The former is called [liquidity bonds](https://docs.otterclam.finance/references/glossary#liquidity-bonds) and the latter [reserve bonds](https://docs.otterclam.finance/references/glossary#reserve-bonds).

Bonds take roughly 15 epochs to vest, and CLAM tokens are vested linearly to the user over that period. Liquidity bonds help the protocol to accumulate and lock liquidity, while reserve bonds allow the protocol to grow its treasury, and thus its RFV faster.

OtterClam offers five types of bonds [on its website](https://app.otterclam.finance/#/bonds):

* [MAI bond](bond_dai.md)
* [CLAM-MAI LP bond](ohm-dai-lp-bond.md)


## **How to Redeem**

Go to [Bond page](https://app.otterclam.finance/#/bonds) and select the bond type you have purchased. Select the "Redeem" tab. Then, click "Claim Rewards" to claim all of your available rewards.

## Reading the Info

![](../../.gitbook/assets/modal.png)

**Balance** is your balance of SLP tokens. This is the asset used to create a bond.

**Bond Price** is the price of CLAM you get from bonding. You can calculate the bond price using the following formulae:

* SLP Bond: \(Value of your SLP token / CLAM you'll get from bonding\)
* MAI Bond: \(Value of your MAI token / CLAM you'll get from bonding\)

**Market Price** is the market price of CLAM.

**You Will Get** tells you how many CLAM you will get from bonding.

**Debt Ratio** measures the total amount of CLAM created from bonds that have yet to be paid out by the protocol. The debt ratio is calculated differently for SLP bond and MAI bond:

* SLP Bond: \(CLAM created from unredeemed bonds / CLAM total supply\)
* MAI Bond: \(CLAM created from unredeemed bonds / CLAM circulating supply\)

**Vesting Term** measures the period a bond takes to fully redeem. This number is in Ethereum blocks. 33110 blocks is approximately 5 days or 15 epochs.

**Discount** is the difference between the bond price and the market price. In the screenshot above, bonding would give you a 10.63% discount versus buying the same amount of CLAM from the market.

![](../../.gitbook/assets/modal_redeem.png)

**Pending Rewards** is the amount of CLAM you are entitled to receive from bonding.

**Claimable Rewards** is the amount of CLAM that you can claim now. This amount keeps increasing as CLAM is vested to you over the bonding period.

**Full Bond Maturation** refers to the Ethereum block when the bond is fully redeemable.

