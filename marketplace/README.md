# Stargaze Marketplace Smart Contract Code Journal

The audit done for these contracts on August 1st, 2022: [Link](https://github.com/oak-security/audit-reports/blob/master/Stargaze/2022-08-01%20Audit%20Report%20-%20Stargaze%20Marketplace%20v1.0.pdf)

A common theme I gathered from reading through the audit is the need for checks and validations. The three major findings dealt mainly with functions found in `execute.rs`. Edge cases are specified, such as those where sellers or bidders may specify an unusually high fee, and the consequences are outlined with regard to the lack of patching the vulnerability.

The difference between major and minor findings seem to deal with vulnerabilities that could unexpectedly lose users money or cause failures. The specific consequences of overflows and underflows are subject to workspace configurations. Type safety reccommendations can be assessed with regards to whether or not those types will need to be used again. If so, I may consider rewriting the implementation in a different spot like they did here in `sudo.rs`.

[![CircleCI](https://circleci.com/gh/public-awesome/marketplace/tree/main.svg?style=svg)](https://circleci.com/gh/public-awesome/marketplace/tree/main)

This repo is under a business source license simliar to Uniswap V3. This means it is **not** available under an open source license for a period of time. Please refer
to [LICENSE](LICENSE) for full details.

# DISCLAIMER

STARGAZE MARKETPLACE IS PROVIDED “AS IS”, AT YOUR OWN RISK, AND WITHOUT WARRANTIES OF ANY KIND. No developer or entity involved in creating or instantiating Stargaze smart contracts will be liable for any claims or damages whatsoever associated with your use, inability to use, or your interaction with other users of Stargaze, including any direct, indirect, incidental, special, exemplary, punitive or consequential damages, or loss of profits, cryptocurrencies, tokens, or anything else of value. Although Public Awesome, LLC and it's affilliates developed the initial code for Stargaze, it does not own or control the Stargaze network, which is run by a decentralized validator set.
