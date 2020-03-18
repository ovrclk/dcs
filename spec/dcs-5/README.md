---
dcs: 5
title: Cosmos SDK Codebase Migration
author: Adam Bozanich (@boz)
status: Final
type: Standards Track
category: Core
discussions-to: https://github.com/ovrclk/akash/issues/457
created: 2020-03-09
updated: 2020-03-17
---

# Summary

Rewrite Akash codebase to [Cosmos SDK](https://docs.cosmos.network) to improve scalability, efficiency, and security.

# Motivation

Reduce the attack footprint and improve maintainability by using audited and battle-tested codebase.

# Rationale

The Akash blockchain development began in 2017 on an older version of Tendermint that proved to unscalable. 

By migrating to Cosmos SDK, we believe Akash can solve the scalability issues and leverage an extensive set of prebuilt modules and audited and battle-tested.

## Copyright

All content herein is licensed under [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).
