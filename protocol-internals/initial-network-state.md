# Initial Network State

**Our initial goal is not to find a stable price.** This may seem antithetical to our currency aspirations, but we ensure you it is not. **OtterClam** can be tuned to optimize for different things. The main tradeoff is volatility and profitability versus stability and consistency. With volatility and profit comes growth; this is what we want early on.

With tight policy and scale, **OtterClam** should function well as a stable asset. Upward and downward pressures should stabilize at some non-intrinsic value. With loose policy, regardless of scale, **OtterClam** has the potential to act as a wealth creation machine. The market premium of the token measures the positive sum of the game; all extrinsic value is new wealth created.

## Alpha State

The initial network features a one-way treasury (money goes in, none comes out), the bonding contract (through which supply increases and profits are produced), and the staking contract (where profits are distributed).

The following are the initial policy states:

*   **BCV**

    [BCV](https://docs.otterclam.finance/references/glossary#bcv) varies based on bond types. It is tuned regularly by the Policy team to meet the protocol goals. For example, if the protocol wants to accumulate more liquidity into its treasury, it can lower the BCV for [liquidity bonds](https://docs.otterclam.finance/references/glossary#liquidity-bonds) to increase their bond capacity.
*   **Bond vesting term**

    It is set to 86400 \* 5 seconds = five days for all bond types.
*   **CLAM distribution**

    Every time someone purchases a bond, the proceed will go to the [OtterClam treasury](https://docs.otterclam.finance/references/contracts#treasury). A corresponding amount of CLAM will be minted and distributed to three parties:

    *   Bonder

        The bond purchaser will receive the quoted amount of CLAM linearly over the vesting term.
    *   DAO

        The DAO receives the same amount of CLAM as the bonder. This represents the DAO profit.
    *   Stakers

        After accounting for the CLAM distributed to the bonder and the DAO, the rest will be distributed among all stakers in the protocol.
