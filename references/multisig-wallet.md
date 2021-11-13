# Multisig Wallet

Our OtterClam DAO contract is guarded by a gnosis safe multisig implementation. The OtterClam DAO gnosis safe address will hold all the treasury funds accumulated. As an example, the OtterClam DAO receives profit from every bond and LP transaction by contract design.

Below is the OtterClam gnosis safe, where the latest version represents the currently active address.

• [0x929A27c46041196e1a49C7B459d63eC9A20cd879](https://polygon.gnosis-safe.io/app/#/safes/0x929A27c46041196e1a49C7B459d63eC9A20cd879)

### Safe Signers

* Otter King(dev): 0x63B0fB7FE68342aFad3D63eF743DE4A74CDF462B
* Dang(dev): 0x1BE4BbAF1b232F5180F2d3306269F8E446bC0A4f
* Joust(mod): 0x67dE004c376Be6a9c44f5EF9d0B4BB35165eA4F9
* Church(mod): 0xC01e6A8df21c7Ae757b0bB8bba95200e8Ec6C518
* QiDao: 0xc96ea79A32Ec5B74A25b15Bb331a03BcFF424d6D

### Policy

The DAO contract is guarded by a 4 of 5 multisig policy. Requiring any transaction to make changes to the DAO must be approved by at least 4 stakeholders of the total 5 stakeholders within the multisig policy.
