# Equations

## Staking

$$
deposit = withdrawal
$$

Swaps between CLAM and sCLAM during staking and unstaking are always honored 1:1. The amount of CLAM deposited into the staking contract will always result in the same amount of sCLAM. And the amount of sCLAM withdrawn from the staking contract will always result in the same amount of CLAM.

$$
harvest = 1 - ( CLAM_{Deposits} / sCLAM_{Outstanding} )
$$

The treasury deposits CLAM into the distributor. The distributor then deposits CLAM into the staking contract, creating an imbalance between CLAM and sCLAM. sCLAM is harvested to correct this imbalance between CLAM deposited and sCLAM outstanding. The harvest brings sCLAM outstanding back up to parity so that 1 sCLAM equals 1 staked CLAM.

## Bonding

$$
bond Price = 1 + Premium
$$

CLAM has an intrinsic value of 1 MAI, which is roughly equivalent to $1. In order to make a profit from bonding, OtterClam charges a premium for each bond.

$$
Premium = debt Ratio * BCV
$$

The premium is derived from the debt ratio of the system and a scaling variable called [BCV](https://docs.otterclam.finance/references/glossary#bcv). BCV allows us to control the rate at which bond prices increase.

The premium determines profit due to the protocol and in turn, stakers. This is because new CLAM is minted from the profit and subsequently distributed among all stakers.

$$
debt Ratio = bondsOutstanding/CLAM_{Supply}
$$

The debt ratio is the total of all CLAM promised to bonders divided by the total supply of CLAM. This allows us to measure the debt of the system.

$$
bondPayout_{reserveBond} = marketValue_{asset}\ /\ bondPrice
$$

Bond payout determines the number of CLAM sold to a bonder. For [reserve bonds](https://docs.otterclam.finance/references/glossary#reserve-bonds), the market value of the assets supplied by the bonder is used to determine the bond payout. For example, if a user supplies 1000 MAI and the bond price is 250 MAI, the user will be entitled 4 CLAM.

$$
bondPayout_{lpBond} = marketValue_{lpToken}\ /\ bondPrice
$$

For [liquidity bonds](https://docs.otterclam.finance/references/glossary#liquidity-bonds), the market value of the LP tokens supplied by the bonder is used to determine the bond payout. For example, if a user supplies 0.001 CLAM-MAI LP token which is valued at 1000 MAI at the time of bonding, and the bond price is 250 MAI, the user will be entitled 4 CLAM.

## CLAM Supply

$$
CLAM_{supplyGrowth} = CLAM_{stakers} + CLAM_{bonders} + CLAM_{DAO} + CLAM_{pCLAMExercise}
$$

CLAM supply does not have a hard cap. Its supply increases when:

* CLAM is minted and distributed to the stakers.
* CLAM is minted for the bonder. This happens whenever someone purchases a bond.
* CLAM is minted for the DAO. This happens whenever someone purchases a bond. The DAO gets the same number of CLAM as the bonder.
* CLAM is minted for the team, investors, advisors, or the DAO. This happens whenever

  the aforementioned party exercises their pCLAM.

$$
CLAM_{stakers} = CLAM_{totalSupply} * rewardRate
$$

At the end of each epoch, the treasury mints CLAM at a set [reward rate](https://docs.otterclam.finance/references/glossary#reward-rate). These CLAM will be distributed to all the stakers in the protocol. You can track the latest reward rate on the [OtterClam Policy dashboard](https://dune.xyz/shadow/OtterClam-Policy).

$$
CLAM_{bonders} = bondPayout
$$

Whenever someone purchases a bond, a set number of CLAM is minted. These CLAM will not be released to the bonder all at once - they are vested to the bonder linearly over time. The bond payout uses a different formula for different types of bonds. Check the [bonding section above](equations.md#bonding) to see how it is calculated.

$$
CLAM_{DAO} = CLAM_{bonders}
$$

The DAO receives the same amount of CLAM as the bonder. This represents the DAO profit.

$$
CLAM_{pClamExercise} = pCLAM + MAI
$$

The individual would supply 1 pCLAM along with 1 MAI to mint 1 CLAM. The pCLAM is subsequently burned.

## Backing per CLAM

$$
CLAM_{backing} = treasuryBalance_{stablecoin} + treasuryBalance_{otherAssets}
$$

Every CLAM in circulation is backed by the Otter's treasury. The assets in the treasury can be divided into two categories: stablecoin and non-stablecoin.

$$
treasuryBalance_{stablecoin} = RFV_{reserveBond} + RFV_{lpBond}
$$

The stablecoin balance in the treasury grows when bonds are sold. [RFV](https://docs.otterclam.finance/references/glossary#rfv) is calculated differently for different bond types.

$$
RFV_{reserveBond} = assetSupplied
$$

For reserve bonds such as MAI bond, the RFV simply equals to the amount of the underlying asset supplied by the bonder.

$$
RFV_{lpBond} = 2sqrt(constantProduct) * (\%\ ownership\ of\ the\ pool)
$$

For LP bonds such as CLAM-MAI bond, the RFV is calculated differently because the protocol needs to mark down its value. Why? The LP token pair consists of CLAM, and each CLAM in circulation will be backed by these LP tokens - there is a cyclical dependency. To safely guarantee all circulating CLAM are backed, the protocol marks down the value of these LP tokens, hence the name _risk-free_ value \(RFV\).

