# BigchainDB Roadmap

Below is a sketch of some of the things we plan to do in upcoming releases of BigchainDB Server (and associated software). It is, of course, subject to change. [This March 2017 medium post](https://blog.bigchaindb.com/bigchaindb-2017-roadmap-d2e7123f9874) gives more context.


## Big-Picture Goals

We're improving BigchainDB along three threads: UX, IPDB, and Core DB.

* Core: improve security, correctness guaranteees, performance, etc.
* UX: Smooth support for user stories. E.g. private payloads, better querying, more
* [IPDB](https://ipdb.foundation/): roll out test net to broader set of users; followed by production net

## Goals for Coming Releases of BigchainDB Server

Note: Each version of BigchainDB Server will be accompanied by a compatible version of the BigchainDB Python Driver.

### Version 0.10 (early Apr 2017)

* Core: Docs on security, stability and correctness that BDB will provide in version 1.0, and some related system tests
* Core: Improved logging for BigchainDB server
* UX: A WebSockets API to retrieve confirmed transactions in real-time.
* UX: Docs on how to deploy BDB on Kubernetes
* IPDB: Developer portal for IPDB test net

### Version 1.0 (early June 2017)

* Core: Recovery: making continuous backups easy, such that “your data is safe” even if a BigchainDB instance gets hacked
* Core: Security assumption is “as good as centralized” but no more; i.e. at the same level as well-secured mainstream databases.
* Core: Setting expectations: well-documented guarantees on what we do and don’t provide with respect to security, stability, and correctness.
* UX: A way to query BigchainDB for data included in a transaction’s payload or asset data.
* UX: Private payloads, including read permissions as assets
* IPDB: continued rollout of test net to more users

### Version 1.1 (early Aug 2017), Version 1.2 (early Oct 2017)

We will release 1.1 and 1.2, but those will be stepping stones to our targets in 1.3.

### Version 1.3 (mid Dec 2017)

* Core: Defense: better walls against the most probable / highest impacting attack vectors. 
* Core: Monitoring: further improved logging and debuggability.
* Core: Security Audits: this will be done once we’ve built at the levels of monitoring, recovery, and defense. Start with crowd-sourced audit; followed by professional security audit providers.
* Core: Security assumption improves because of the improvements to defense, monitoring, and audits. So the new level is “decentralized is better”: with each new decentralized node, security improves on some dimensions. 
* IPDB: test net open to public
* IPDB: early adopter users shipping on production net
* IPDB: caretaker portal

### Other Future Stuff

We have a large list of possible features, for UX and otherwise. Some may appear in a 1.0 or 1.3 timeframe; and some later. Here's a few of them.

* Improved querying support
* More performance benchmarking & optimization
* Asset policies, i.e. data that carries a policy
* Composable assets, i.e. can group many assets together
* Improved http api
* and more



