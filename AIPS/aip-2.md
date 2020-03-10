---
aip: 2
title: Provider Accreditation
author: Greg Osuri (@gosuri)
status: Idea
type: Standards Track
category: Core
created: 2020-03-09
---

# Summary
Implement a set of changes that improves a tenant's trust for a provider in a trust minimized setting.


## Rationale
Akash is a permission-less network where any tenant (with a valid key) can consume computing services from any provider that has the sufficient computing power in a peer-to-peer manner disintermediating a broker. This provides a challenge for filtering out bad actors. We propose a system where the tenant can delegate the attestation to a trusted third-party (Oracle) with an ability for tenants to selectively deploy to such trusted providers. 

## Specification

1. The accreditor is a publicly trusted third-party where there is pre-established trust with the Provider and Tenant. Anyone with enough public trust can be an accreditor on Akash without needing permission. A PGP web of trust model could be adopted.
2. The accreditor publishes a signed map of trusted providers and attributes on to the chain.
3. The Tenant specifies the Authority (public key of Accreditor) in deployment manifest along with attributes to be verified.
4. The system then limits the auction only to the trusted providers verified by the accreditor (authority).

![Provider accredation](../assets/aip-2/wot.svg)
