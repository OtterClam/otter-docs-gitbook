# Staking

## Distributor

The distributor contract receives minted CLAM from the treasury in order to drip-feed rewards to stakers. The reward rate target as of time of writing is set to 3500, which translates to 0.35% of total supply, since the reward rate is defined in tens of thousands. Note that the reward rate determines the harvest rate and that the harvest rate determines the APY. Below are listed distributor contracts by version, where the latest version represents the currently active contract.

* v2 [0x0Dd0...FC62](https://polygonscan.com/address/0x0Dd015889df6F50d39e9D7A52711D0B86E43FC62)

## Staking

Prior to the migration of the staking contract, the old staking contract \([0xcF2A...0dBf](https://polygonscan.com/address/0xcF2A11937A906e09EbCb8B638309Ae8612850dBf/)\) was used for staking CLAM. If users are still staked in there they should migrate their staked CLAM to the new staking contract \([0xC8B....221a](https://polygonscan.com/address/0xC8B0243F350AA5F8B979b228fAe522DAFC61221a)\). The new staking contract works with a staking helper contract \([0x76B3....1691](https://polygonscan.com/address/0x76B38319483b570B4BCFeD2D35d191d3c9E01691)\). The staking helper contract calls "stake" and then "claim" of the new staking contract. When the "stake" function is called, sCLAM is put into a warmup phase and all the information about how much sCLAM a user has staked is stored in the new staking contract. When the "claim" function is called, sCLAM is retrieved from the warmup and then sent to the user's wallet.

