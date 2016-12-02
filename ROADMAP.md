# BigchainDB Roadmap

This is a sketch of some of the things we plan to do in upcoming releases of BigchainDB Server (and associated software). It is, of course, subject to change.


## Big-Picture Goals

* Make it easier for developers to code an app that communicates with a BigchainDB cluster (often a cluster run by others). This means improvements to the client-server communications protocol and drivers for building client-side apps.
* Help [IPDB](https://ipdb.foundation/) (a public BigchainDB cluster) become production-grade.
* Convert all RethinkDB-specific code to abstract database calls.
* Write two implementations of all abstract database calls: RethinkDB and [MongoDB](https://www.mongodb.com/).
* Do more performance benchmarking.
 

## Goals for Coming Releases of BigchainDB Server

Note: Each version of BigchainDB Server will be accompanied by a compatible version of the BigchainDB Python Driver.

### Version 0.9

* BigchainDB Transaction Model, Version 1.0 Spec
* BigchainDB HTTP API, Version 1.0 Spec
* BigchainDB Python Driver, Version 1.0 Spec
* BigchainDB Websocket API, Version 1.0 Spec
* Implementations of all the above specs (except maybe not the Websocket API)

### Version 0.10

* JavaScript Driver, Version 1.0 Spec
* Reproduce some reported pain points with performance to understand why (high memory usage and/or slow). Was it their setup? Is it the algorithm?
* Improve performance / instructions / setup (in follow-up to the above point)

### Version 0.11

* Design user experience for read permissions support (payload), e.g. using encryption
* Implement read permissions support (see last point)

### Some Future Things

(This list is just a subset. It will change a lot. The order means nothing.)

* Federation dashboard v1: measure number of weekly active users
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
* More performance benchmarking
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
