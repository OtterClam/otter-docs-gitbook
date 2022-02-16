# FAQ

## Why do we need OtterClam in the first place?



Dollar-pegged stablecoins have become an essential part of crypto due to their lack of volatility as compared to tokens such as Bitcoin and Ether. Users are comfortable with transacting using stablecoins knowing that they hold the same amount of purchasing power today vs. tomorrow. But this is a fallacy. The dollar is controlled by the US government and the Federal Reserve. This means a depreciation of the dollar also means a depreciation of these stablecoins.

OtterClam aims to solve this by creating a free-floating reserve currency, **CLAM**, which is backed by a basket of assets. By focusing on supply growth rather than price appreciation, OtterClam hopes that **CLAM** can function as a currency that can hold its purchasing power regardless of market volatility.

As one of the oldest currencies humans used, we would like to present CLAM as the first store of value that fully integrates DeFi reserve currency tokenomics with a permissionless, open-source NFT platform on the Polygon network.

## Is CLAM a stable coin?

No, **CLAM** is not a stable coin. Rather, **CLAM** aspires to become an algorithmic reserve coin backed by other decentralized assets. Similar to the idea of the gold standard, **CLAM** provides free-floating value its users can always fall back on, simply because of the fractional treasury reserves CLAM draws its intrinsic value from.

## CLAM is backed, not pegged.

Each **CLAM** is backed by 1 MAI, not pegged to it. Because the treasury backs every **CLAM** with at least 1 MAI, the protocol would buy back and burn **CLAM** when it trades below 1 MAI. This has the effect of pushing the **CLAM** price back up to 1 MAI. **CLAM** could always trade above 1 MAI because there is no upper limit imposed by the protocol. Think pegged == 1, while backed >= 1.

You might say that the **CLAM** floor price or intrinsic value is 1 MAI. We believe that the actual price will always be 1 MAI + premium, but in the end that is up to the market to decide.

## How does it work?

At a high level, OtterClam consists of its protocol managed treasury, protocol owned liquidity ([POL](../references/glossary.md#pol)), bond mechanism, and staking rewards that are designed to control supply expansion.

Bond sales generate profit for the protocol, and the treasury uses the profit to mint **CLAM** and distribute them to stakers. With [liquidity bonds](../references/glossary.md#liquidity-bonds), the protocol is able to accumulate its own liquidity. Check out the entry below on [the importance of POL](faq.md#why-is-pol-important).

## What is the deal with (🦦,🦦) and (![](../.gitbook/assets/favicon@2x.png),![](../.gitbook/assets/favicon@2x.png))?

(🦦,🦦) is the idea that, if everyone love otters, it would generate the greatest gain for everyone (from a [game theory](https://en.wikipedia.org/wiki/Game\_theory) standpoint). Currently, there are three actions a user can take:

* Staking (🦦)

Bonding (![](../.gitbook/assets/favicon@2x.png))

* Selling (💀)

Staking and bonding are considered beneficial to the protocol, while selling is considered detrimental. Staking and selling will also cause a price move, while bonding does not (we consider buying CLAM from the market as a prerequisite of staking, thus causing a price move). If both actions are beneficial, the actor who moves price also gets half of the benefit (![](../.gitbook/assets/favicon@2x.png)). If both actions are contradictory, the bad actor who moves price gets half of the benefit (![](../.gitbook/assets/favicon@2x.png)), while the good actor who moves price gets half of the downside (💀). If both actions are detrimental, which implies both actors are selling, they both get half of the downside (💀).

Thus, given two actors, all scenarios of what they could do and the effect on the protocol are shown here:

![](../.gitbook/assets/game\_theory.jpg)

* If we both stake (🦦, 🦦), it is the best thing for both of us and the protocol. The otters will harvest more **CLAM** tokens for us.
* If one of us stakes and the other one bonds, it is also great because staking takes **CLAM** off the market and puts it into the protocol, while bonding provides liquidity and MAI for the treasury.
* When one of us sells, it diminishes the effort of the other one who stakes or bonds.
* When we both sell, it creates the worst outcome for both of us and the protocol (💀,💀).

## Why is PCV important?

As the protocol controls the funds in its treasury, **CLAM** can only be minted or burned by the protocol. This also guarantees that the protocol can always back 1 **CLAM** with 1 MAI. You can easily define the risk of your investment because you can be confident that the protocol will indefinitely buy **CLAM** below 1 MAI with the treasury assets until no one is left to sell. You can't trust the FED but you can trust the code.

As the protocol accumulates more PCV, more runway is guaranteed for the stakers. This means the stakers can be confident that the current staking APY can be sustained for a longer term because more funds are available in the treasury.

## Why is the market price of CLAM so volatile?

It is extremely important to understand how early in development the OtterClam protocol is. A large amount of discussion has centered around the current price and expected a stable value moving forward. The reality is that these characteristics are not yet determined. The network is currently tuned for expansion of **CLAM** supply, which when paired with the staking, bonding, and yield mechanics of OtterClam, result in a fair amount of volatility.

**CLAM** could trade at a very high price because the market is ready to pay a hefty premium to capture a percentage of the current market capitalization. However, the price of **CLAM** could also drop to a large degree if the market sentiment turns bearish. We would expect significant price volatility during our growth phase so please **do your own research** whether this project suits your goals.

## What is the point of buying CLAM if it is trading at a very high premium?

When you buy and stake **CLAM**, you capture a percentage of the supply (market cap) that will remain close to a constant. This is because your staked **CLAM** balance also increases along with the circulating supply. The implication is that if you buy **CLAM** when the market cap is low, you would be capturing a larger percentage of the market cap.

## What is a harvest?

Harvest is a mechanism by which your staked **CLAM** balance increases automatically. When new **CLAM** are minted by the protocol, a large portion of it goes to the stakers. Because stakers only see staked **CLAM** balance instead of **CLAM**, the protocol utilizes the harvesting mechanism to increase the staked **CLAM** balance so that 1 staked CLAM is always redeemable for 1 **CLAM**.

## What is reward yield?

Reward yield is the percentage by which your staked **CLAM** balance increases during the next epoch. It is also known as _harvest rate_. You can find this number on the [OtterClam staking page](https://app.otterclam.finance/#/stake).

## What is APY?

APY stands for annual percentage yield. It measures the real rate of return on your principal by taking into account the effect of compounding interest. In the case of OtterClam, your staked **CLAM** represents your principal, and the compound interest is added periodically on every epoch (8 hours) thanks to the harvesting mechanism.

One interesting fact about APY is that your balance will grow not linearly but exponentially over time! Assuming a daily compound interest of 2%, if you start with a balance of 1 **CLAM** on day 1, after a year, your balance will grow to about 1377. That is a lot!

![The power of compounding](../.gitbook/assets/apy.png)

## How is the APY calculated?

The APY is calculated from the reward yield (a.k.a harvest rate) using the following equation:

$$
APY = ( 1 + rewardYield )^{1095}
$$

It raises to the power of 1095 because a harvest happens 3 times daily. Consider there are 365 days in a year, this would give a harvesting frequency of 365 \* 3 = 1095.

Reward yield is determined by the following equation:

$$
rewardYield = CLAM_{distributed} / CLAM_{totalStaked}
$$

The number of CLAMs distributed to the staking contract is calculated from CLAM total supply using the following equation:

$$
CLAM_{distributed} = CLAM_{totalSupply} \times rewardRate
$$

Note that the reward rate is subject to change by the protocol.

## Why does the price of CLAM become irrelevant over the long term?

As illustrated above, your CLAM balance will grow exponentially over time thanks to the power of compounding. Let's say you buy a **CLAM** for $400 now and the market decides that in 1 year's time, the intrinsic value of **CLAM** will be $2. Assuming a daily compound interest rate of 2%, your balance would grow to about 1377 **CLAMs** by the end of the year, which is worth around $2754. That is a cool $2354 profit! By now, you should understand that you are paying a premium for **CLAM** now in exchange for a long-term benefit. Thus, you should have a long time horizon to allow your **CLAM** balance to grow exponentially and make this a worthwhile investment.

## What will be CLAM's intrinsic value in the future?

There is no clear answer for this, but the intrinsic value can be determined by treasury performance. For example, if the treasury could guarantee to back every **CLAM** with 100 MAI, the intrinsic value will be 100 MAI. It can also be decided by the DAO. For example, if the DAO decides to raise the price floor of **CLAM**, its intrinsic value will rise accordingly.

## How does the protocol manage to maintain the high staking APY?

Let’s say the protocol targets an APY of 100,000%. This would translate to a harvest rate of about 0.6328%, or a daily growth of about 2%. Please refer to the equation above to learn [how APY is calculated from the harvest rate](faq.md#how-is-the-apy-calculated).

If there are 100,000 **CLAM** staked right now, the protocol would need to mint an additional 2000 **CLAM** to achieve this daily growth. This is achievable if the protocol can bring in at least 2000 MAI daily from bond sales. If the protocol fails to achieve this, the APY of 100,000% cannot be guaranteed.

## Do I have to unstake and stake CLAM on every epoch to get my harvest rewards?

No. Once you have staked **CLAM** with OtterClam, your staked **CLAM** balance will auto-compound on every epoch. That increase in balance represents your harvest rewards.

## How do I track my harvest rewards?

You can track your harvest rewards by calculating the increase in your staked **CLAM** balance.

1. Record down the Current Index value on the [staking page](https://app.otterclam.finance/#/) when you first stake your **CLAM**. Let's call this the Start Index.
2. After staking for some time, if you want to determine by how much your balance has increased, check the Current Index value again. Let's call this the End Index.
3. By dividing the End Index by Start Index, you would get the ratio by which your staked **CLAM** balance has increased.

$$
ratio = endIndex / startIndex
$$

1. In this example, the CLAM balance has grown by 1.5 times.

$$
ratio = 13.2\ /\ 8.8\newline = 1.5
$$

## Is OtterClam Audited?

[The first audit by SlowMist](https://www.slowmist.com/en/security-audit-certificate.html?id=4d43b0eb547aa83dc2ff5bef71f99916e33b669a5f30572f1826d7e8220265c2) was completed on the 15th of December 2021. It covered all deployed smart contracts at the time.
