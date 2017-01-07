# BigchainDB Roadmap

This is a sketch of some of the things we plan to do in upcoming releases of BigchainDB Server (and associated software). It is, of course, subject to change.


## Big-Picture Goals

We're improving BigchainDB along three threads: UX, IPDB, and Core DB.

* UX: Smooth support for user stories. E.g. private payloads, better querying, more. Improvements may be at the level of transaction (a JSON schema), http api, or driver (python, CLI, JS, etc.). 
* [IPDB](https://ipdb.foundation/): help this public BigchainDB cluster become production-grade. 
* Core DB: Support [MongoDB](https://www.mongodb.com/), improve performance, improve security

## Goals for Coming Releases of BigchainDB Server

Note: Each version of BigchainDB Server will be accompanied by a compatible version of the BigchainDB Python Driver.

### Version 0.9

* Well-defined spec (with implementation) for each of: BDB transaction model, http api, python driver

### Version 0.10

* MongoDB support (maybe released sooner)
* JS driver
* Improved quering support

### Version 0.11

* Private payloads, including read permissions as assets

### Some Future Things

(This list is just a subset. It will change a lot. The order means nothing.)

* IPDB Testnet developer portal where one can sign up for an account, get an access token, see usage statistics, etc.
* Docs: streamlined onboarding from bigchaindb.com, for app developers
* Initial ARM (Azure Resource Manager) template to provision a production node on Azure
* Docs for onboarding from ipdb.foundation website
* IPDB billing
* Node-monitoring dashboard
* Document what security guarantees we provide and don't provide
* Continued work on adding support for MongoDB: many aspects
* DSL/Querying v1 definition.
* DSL or similar means to compose crypto-conditions
* More performance benchmarking & optimization
* More whole-system _correctness_ tests


## Some Repository-Specific GitHub Links

| **Repository** | **Open issues** | **Open PRs** |
|----------------|-----------------|--------------|
| BigchainDB Server | [Open issues](https://github.com/bigchaindb/bigchaindb/issues) | [Open PRs](https://github.com/bigchaindb/bigchaindb/pulls) |
| BigchainDB Python Driver | [Open issues](https://github.com/bigchaindb/bigchaindb-driver/issues) | [Open PRs](https://github.com/bigchaindb/bigchaindb-driver/pulls) |
| bigchaindb/cryptoconditions | [Open issues](https://github.com/bigchaindb/cryptoconditions/issues) | [Open PRs](https://github.com/bigchaindb/cryptoconditions/pulls) |
| This repository | [Open issues](https://github.com/bigchaindb/org/issues) | [Open PRs](https://github.com/bigchaindb/org/pulls) |


## Waffle Board

We have [a "waffle board" (on waffle.io)](https://waffle.io/bigchaindb/org/) which gives a high-level overview of all issues and pull requests from across all BigchainDB repositories on GitHub. You may find it interesting. The **Done** column is things closed in the last week. **New PRs + R-Issues (ref'd by new branches)** is an auto-populated column listing 1) new pull requests and 2) issues where a new branch referencing that issue was created.
