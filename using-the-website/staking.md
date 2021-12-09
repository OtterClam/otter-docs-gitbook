# 🦦 Stake Your CLAM

Staking allows you to passively earn CLAM via auto-compounding. By staking your CLAM with OtterClam, you receive sCLAM (staked CLAM) in return at a 1:1 ratio. After that, your sCLAM balance will automatically increase on every epoch based on the current APY.

## How to Buy CLAM

{% hint style="warning" %}
Buy CLAM on: [Quickswap](https://quickswap.exchange/#/swap?outputCurrency=0xC250e9987A032ACAC293d838726C511E6E1C029d). Make sure to **check the slippage first** before buying CLAM, as some venues offer a worse rate than others due to low liquidity.
{% endhint %}

1. Go to [this Sushiswap swap page](https://app.sushi.com/swap?outputCurrency=0x383518188c0c6d7730d91b2c03a03c837814a899). We use Sushiswap as an example here. We recommend that you should compare the exchange rate across different DEXes to ensure you are getting the best price.
2. Make sure the output currency is CLAM. You can also copy and paste the [CLAM contract address](broken-reference) into the output currency field to ensure you are swapping for the right token.

![Paste CLAM contract address](../.gitbook/assets/ohm\_contract.png)

1. You can select any input currency based on your available wallet balance.  We recommend that you use MAI as the input currency to lower slippage.

![Make sure the output currency is CLAM](../.gitbook/assets/buy\_ohm.png)

1. Select the amount of CLAM you want to swap for. Then click "Approve" and sign the transaction.
2. After the "Approve" transaction has been processed successfully, click "Swap" and sign the transaction.
3. You should see CLAM in your wallet balance now after the swap transaction is successful. If you cannot find it in your wallet, add [CLAM contract address](broken-reference) to your wallet.

{% hint style="info" %}
The "Approve" transaction is only needed when you swap CLAM for the first time. Any swapping after the first one only requires you to perform the "Swap" transaction.
{% endhint %}

## How to Stake

1. Go to the [Stake page of the OtterClam website](https://app.otterclam.finance/#/stake). Select the "Stake" tab.
2. Enter the amount of CLAM that you would like to stake in the input field. If you would like to stake all your CLAM, press the "Max" button. This will populate the input field with all your available CLAM balance.
3. Click "Approve" and sign the transaction.
4. After the "Approve" transaction has been processed successfully, click "Stake" and sign the transaction. Voila, you have staked your CLAM!

## How to Unstake

1. Go to the [Stake page of the OtterClam website](https://app.otterclam.finance/#/stake). Select the "Unstake" tab.
2. Enter the amount of sCLAM that you would like to unstake in the input field. If you would like to unstake all your sCLAM, press the "Max" button. This will populate the input field with all your available sCLAM balance. 
3. Click "Approve" and sign the transaction.
4. After the "Approve" transaction has been processed successfully, click "Unstake" and sign the transaction.

_Note: The "Approve" transaction is only needed when staking/unstaking for the first time; subsequent staking/unstaking only requires you to perform the "Stake" or "Unstake" transaction._

## Reading the Info

![The staking page](../.gitbook/assets/staking\_page\_index.png)

**APY** tells you the annualized rate of return based on the reward yield. It takes into account the effect of compounding since sCLAM harvests exponentially.

**TVL** measures the dollar amount of all the staked CLAM in OtterClam.

**Current Index** allows you to track your gain from staking. The index started from 1 at epoch 0 and increases every epoch. If you staked at genesis (epoch 0) and never unstaked any CLAM, your balance today would be X times greater, where X is the current index. You can use the index to track your position by marking down the index number when you stake and unstake. You divide the index number when you unstake by the index number when you stake to get the ratio by which your sCLAM balance has increased.

**Your Balance** tells you how many unstaked CLAMs are in your wallet. This is the largest amount that you can stake.

**Your Staked Balance** tells you how many staked CLAMs are in your wallet. This is the largest amount that you can unstake.

**Next Harvest** tells you the remaining time until the next harvest.

**Reward Yield** tells you how much your sCLAM balance will increase when the next epoch begins. For example, if you stake 100 CLAM and the upcoming harvest is 0.5%, your sCLAM balance would increase from 100 to 100.5.

**ROI (5-Day Rate)** estimates how much your sCLAM balance will increase after 5 days if the reward yield stays the same during this period. For example, if you stake 100 CLAM and the rate is 8.5%, your sCLAM balance would increase from 100 to 108.5 after 5 days.
