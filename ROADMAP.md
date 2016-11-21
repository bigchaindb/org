# BigchainDB Roadmap

This is a sketch of some of the things we plan to do in upcoming releases of BigchainDB Server (and associated software). It is, of course, subject to change.


## Big-Picture Goals

* Make it easier for developers to code an app that communicates with a BigchainDB cluster (often a cluster run by others). This means improvements to the client-server communications protocol and drivers for building client-side apps.
* Help [IPDB](https://ipdb.foundation/) (a public BigchainDB cluster) become production-grade.
* Convert all RethinkDB-specific code to code that has the database backend as a parameter.
* Add support for a second database backend: [MongoDB](https://www.mongodb.com/).
* Build the [Wire Protocol Firewall](https://github.com/bigchaindb/bigchaindb/issues/594) for MongoDB.
* Do more performance benchmarking.
 

## Goals for Coming Releases of BigchainDB Server

Note: Each version of BigchainDB Server will be accompanied by a compatible version of the BigchainDB Python Driver.

### Version 0.8

* Have the IPDB Testnet up and running for select third parties
* Have a form where developers can sign up for access to the IPDB Testnet
* Convert all core-code RethinkDB queries (CRUD) into abstract queries
* Implement the MongoDB versions of all core-code database queries
* Support for divisible assets
* (Python Driver) Separate methods to build, sign and push transactions


### Version 0.9

* Some way to restrict access to the HTTP API
* Federation dashboard v1: measure number of weekly active users
* Single DNS hostname for HTTP API (with load balancer?)
* Initial ARM (Azure Resource Manager) template to provision a production node on Azure
* Docs: streamlined onboarding from bigchaindb.com, for app developers
* Abstract RethinkDB code in all tests
* Implement the MongoDB versions of all database calls made in the tests
* Abstract the code to set up the RethinkDB database (tables, indexes, etc.)
* Implement the MongoDB code to set up the database
* Write a formal specification of the transaction data model, used to power transaction schema validation
* Ability to get all transactions associated with a given public key (client side)
* Tooling to compose crypto-conditions


### Version 0.10

(This list will probably change _a lot_.)

* More dashboards work (node and cluster)
* More MongoDB support work
* Start work on the MongoDB wire protocol Firewall
* Start work on support for permissions & roles


## Some Repository-Specific GitHub Links

| **Repository** | **Open issues** | **Open PRs** |
|----------------|-----------------|--------------|
| BigchainDB Server | [Open issues](https://github.com/bigchaindb/bigchaindb/issues) | [Open PRs](https://github.com/bigchaindb/bigchaindb/pulls) |
| BigchainDB Python Driver | [Open issues](https://github.com/bigchaindb/bigchaindb-driver/issues) | [Open PRs](https://github.com/bigchaindb/bigchaindb-driver/pulls) |
| bigchaindb/cryptoconditions | [Open issues](https://github.com/bigchaindb/cryptoconditions/issues) | [Open PRs](https://github.com/bigchaindb/cryptoconditions/pulls) |
| This repository | [Open issues](https://github.com/bigchaindb/org/issues) | [Open PRs](https://github.com/bigchaindb/org/pulls) |


## Waffle Board

We have [a "waffle board" (on waffle.io)](https://waffle.io/bigchaindb/org/) which gives a high-level overview of all issues and pull requests from across all BigchainDB repositories on GitHub. You may find it interesting. The **Done** column is things closed in the last week. **New PRs + R-Issues (ref'd by new branches)** is an auto-populated column listing 1) new pull requests and 2) issues where a new branch referencing that issue was created.
