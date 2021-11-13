# Staking

## Distributor

The distributor contract receives minted CLAM from the treasury in order to drip-feed rewards to stakers. The reward rate target as of time of writing is set to 3500, which translates to 0.35% of total supply, since the reward rate is defined in tens of thousands. Note that the reward rate determines the harvest rate and that the harvest rate determines the APY. Below are listed distributor contracts by version, where the latest version represents the currently active contract.

* V1 [0xbe73...242f](https://etherscan.io/address/0xbe731507810C8747C3E01E62c676b1cA6F93242f)

## Staking

Prior to the migration of the staking contract, the old staking contract \([0x0822...74A2](https://etherscan.io/address/0x0822F3C03dcc24d200AFF33493Dc08d0e1f274A2)\) was used for staking CLAM. If users are still staked in there they should migrate their staked CLAM to the new staking contract \([0xFd31....566a](https://etherscan.io/address/0xFd31c7d00Ca47653c6Ce64Af53c1571f9C36566a)\). The new staking contract works with a staking helper contract \([0xC8C4....612d](https://etherscan.io/address/0xC8C436271f9A6F10a5B80c8b8eD7D0E8f37a612d)\). The staking helper contract calls "stake" and then "claim" of the new staking contract. When the "stake" function is called, sCLAM is put into a warmup phase and all the information about how much sCLAM a user has staked is stored in the new staking contract. When the "claim" function is called, sCLAM is retrieved from the warmup and then sent to the user's wallet.

