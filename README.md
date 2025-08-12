1. Relative Stability: Anchored or pegged -> $1.00
   1. Chainlink price feed.
   2. Set a function to exchange ETH to BTC -> $$$
2. Stability Mechanism (Minting): Algorithmic (Decentralized)
   1. People can only mint the stablecoin with enough collateral (coded)
3. Collateral: Exogenous(Crypto)
   1. wEth
   2. wBTC
<!-- COVERAGE-START -->
## Solidity Coverage Report

```
Compiling 44 files with Solc 0.8.30
Solc 0.8.30 finished in 2.23s
Compiler run successful with warnings:
Warning (3420): Source file does not specify required compiler version! Consider adding "pragma solidity ^0.8.30;"
--> test/fuzz/InvariantsTest.t.sol

Analysing contracts...
Running tests...

Ran 40 tests for test/unit/DSCEngine.t.sol:DSCEngineTest
[PASS] testCanBurnDsc() (gas: 241889)
[PASS] testCanDepositCollateralGetAccountInfo() (gas: 137908)
[PASS] testCanDepositCollateralWithoutMinting() (gas: 88691)
[PASS] testCanMinDsc() (gas: 206701)
[PASS] testCanMintWithDepositedCollateral() (gas: 205295)
[PASS] testCanRedeemCollateral() (gas: 132258)
[PASS] testCanRedeemDepositedCollateral() (gas: 259025)
[PASS] testCantBurnMoreThanUserHas() (gas: 13926)
[PASS] testCantLiquidateGoodHealthFactor() (gas: 365836)
[PASS] testEmitCollateralRedeemedWithCorrectArgs() (gas: 130340)
[PASS] testGetAccountCollateralValue() (gas: 129357)
[PASS] testGetAccountCollateralValueFromInformation() (gas: 131948)
[PASS] testGetCollateralBalanceOfUser() (gas: 84053)
[PASS] testGetCollateralTokenPriceFeed() (gas: 16067)
[PASS] testGetCollateralTokens() (gas: 19894)
[PASS] testGetDsc() (gas: 11245)
[PASS] testGetLiquidationThreshold() (gas: 9009)
[PASS] testGetMinHealthFactor() (gas: 8918)
[PASS] testGetTokenAmountFromUsd() (gas: 33814)
[PASS] testGetUsdValue() (gas: 28534)
[PASS] testHealthFactorCanGoBelowOne() (gas: 294409)
[PASS] testLiquidationPayoutIsCorrect() (gas: 516757)
[PASS] testLiquidationPrecision() (gas: 8911)
[PASS] testLiquidatorTakesOnUsersDebt() (gas: 508288)
[PASS] testMustImproveHealthFactorOnLiquidation() (gas: 3352594)
[PASS] testMustRedeemMoreThanZero() (gas: 241130)
[PASS] testProperlyReportsHealthFactor() (gas: 214671)
[PASS] testRevertsIfBurnAmountIsZero() (gas: 202586)
[PASS] testRevertsIfCollateralZero() (gas: 43336)
[PASS] testRevertsIfMintAmountBreaksHealthFactor() (gas: 172938)
[PASS] testRevertsIfMintAmountIsZero() (gas: 202432)
[PASS] testRevertsIfMintFails() (gas: 2973213)
[PASS] testRevertsIfMintedDscBreaksHealthFactor() (gas: 171163)
[PASS] testRevertsIfRedeemAmountIsZero() (gas: 204012)
[PASS] testRevertsIfTokenLengthDoesntMatchPriceFeeds() (gas: 184973)
[PASS] testRevertsIfTransferFails() (gas: 2849750)
[PASS] testRevertsIfTransferFromFails() (gas: 2873457)
[PASS] testRevertsWithUnapprovedCollateral() (gas: 952007)
[PASS] testUserHasNoMoreDebt() (gas: 508260)
[PASS] testUserStillHasSomeEthAfterLiquidation() (gas: 535206)
Suite result: ok. 40 passed; 0 failed; 0 skipped; finished in 18.07ms (25.68ms CPU time)

Ran 2 tests for test/fuzz/Invariants.t.sol:InvariantTest
[PASS] invariant_gettersShouldNotRevert() (runs: 128, calls: 16384, reverts: 0)

╭----------+-------------------+-------+---------+----------╮
| Contract | Selector          | Calls | Reverts | Discards |
+===========================================================+
| Handler  | depositCollateral | 5573  | 0       | 0        |
|----------+-------------------+-------+---------+----------|
| Handler  | mintDsc           | 5452  | 0       | 0        |
|----------+-------------------+-------+---------+----------|
| Handler  | redeemCollateral  | 5359  | 0       | 0        |
╰----------+-------------------+-------+---------+----------╯

[PASS] invariant_protocolMustHaveMoreValueThanTotalSupply() (runs: 128, calls: 16384, reverts: 0)

╭----------+-------------------+-------+---------+----------╮
| Contract | Selector          | Calls | Reverts | Discards |
+===========================================================+
| Handler  | depositCollateral | 5470  | 0       | 0        |
|----------+-------------------+-------+---------+----------|
| Handler  | mintDsc           | 5543  | 0       | 0        |
|----------+-------------------+-------+---------+----------|
| Handler  | redeemCollateral  | 5371  | 0       | 0        |
╰----------+-------------------+-------+---------+----------╯

Suite result: ok. 2 passed; 0 failed; 0 skipped; finished in 8.01s (14.71s CPU time)

Ran 2 test suites in 8.01s (8.03s CPU time): 42 tests passed, 0 failed, 0 skipped (42 total tests)
Wrote LCOV report.

╭---------------------------------------+------------------+------------------+---------------+----------------╮
| File                                  | % Lines          | % Statements     | % Branches    | % Funcs        |
+==============================================================================================================+
| script/DeployDSC.s.sol                | 0.00% (0/12)     | 0.00% (0/14)     | 100.00% (0/0) | 0.00% (0/1)    |
|---------------------------------------+------------------+------------------+---------------+----------------|
| script/HelperConfig.s.sol             | 75.00% (12/16)   | 82.35% (14/17)   | 33.33% (1/3)  | 66.67% (2/3)   |
|---------------------------------------+------------------+------------------+---------------+----------------|
| src/DSCEngine.sol                     | 0.00% (0/118)    | 0.00% (0/110)    | 0.00% (0/10)  | 0.00% (0/33)   |
|---------------------------------------+------------------+------------------+---------------+----------------|
| src/DecentralizedStableCoin.sol       | 71.43% (10/14)   | 69.23% (9/13)    | 0.00% (0/4)   | 100.00% (2/2)  |
|---------------------------------------+------------------+------------------+---------------+----------------|
| src/libraries/OracleLib.sol           | 100.00% (6/6)    | 85.71% (6/7)     | 0.00% (0/1)   | 100.00% (1/1)  |
|---------------------------------------+------------------+------------------+---------------+----------------|
| test/fuzz/Handler.t.sol               | 95.12% (39/41)   | 95.35% (41/43)   | 75.00% (3/4)  | 100.00% (5/5)  |
|---------------------------------------+------------------+------------------+---------------+----------------|
| test/mocks/ERC20Mock.sol              | 40.00% (4/10)    | 40.00% (2/5)     | 100.00% (0/0) | 40.00% (2/5)   |
|---------------------------------------+------------------+------------------+---------------+----------------|
| test/mocks/MockFailedMintDSC.sol      | 35.71% (5/14)    | 30.77% (4/13)    | 0.00% (0/4)   | 50.00% (1/2)   |
|---------------------------------------+------------------+------------------+---------------+----------------|
| test/mocks/MockFailedTransfer.sol     | 36.36% (4/11)    | 22.22% (2/9)     | 0.00% (0/2)   | 66.67% (2/3)   |
|---------------------------------------+------------------+------------------+---------------+----------------|
| test/mocks/MockFailedTransferFrom.sol | 36.36% (4/11)    | 22.22% (2/9)     | 0.00% (0/2)   | 66.67% (2/3)   |
|---------------------------------------+------------------+------------------+---------------+----------------|
| test/mocks/MockMoreDebtDSC.sol        | 76.47% (13/17)   | 73.33% (11/15)   | 0.00% (0/4)   | 100.00% (3/3)  |
|---------------------------------------+------------------+------------------+---------------+----------------|
| test/mocks/MockV3Aggregator.sol       | 52.17% (12/23)   | 52.94% (9/17)    | 100.00% (0/0) | 50.00% (3/6)   |
|---------------------------------------+------------------+------------------+---------------+----------------|
| Total                                 | 37.20% (109/293) | 36.76% (100/272) | 11.76% (4/34) | 34.33% (23/67) |
╰---------------------------------------+------------------+------------------+---------------+----------------╯
```
<!-- COVERAGE-END -->
