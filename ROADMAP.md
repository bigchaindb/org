# BigchainDB Roadmap

Below is a sketch of some of the things we plan to do in upcoming releases of BigchainDB Server (and associated software), i.e. in the near term. It is, of course, subject to change.

If you don't see your important feature listed here, please read about how to request a feature in our docs on [Contributing to BigchainDB](https://docs.bigchaindb.com/projects/contributing/en/latest/index.html).

## BigchainDB 2.0

### Done for BigchainDB 2.0.0 Alpha (Released on April 3, 2018)

1. Finish HTTP API changes
1. Simplify & automate the production deployment process
1. Consolidate the proposal system (especially COSS)
1. Change the allowed transaction version number from "1.0" to "2.0"
1. Update the official drivers (Python driver & JavaScript driver)
1. BigchainDB Server CLI updates (not the client-side CLI: deprecate that)
1. Compute an app hash for Tendermint (in a dumb way _that works_).
1. Standard process to set up a local node for development & testing, using Docker Compose.
1. Set up a network for the AE team to do some performance tests.
1. New `bigchaindb upsert-validator` subcommand to add/change/remove a validator at run time, "insecure" way.
1. The Events API ane Events Plugin API: update code & docs.

## BigchainDB 2.0 TODO

We intend to do some intermediate releases, e.g. 2.0 Beta, 2.0 RC1 before releasing the final BigchainDB 2.0.0.

- Resolve known issues and bugs.
- Support for metadata search in the Python driver.
- Write about how a node operator can expose the full power of MongoDB to users. For example, they could allow users to make any valid MongoDB query.
- Update Ansible & Vagrant deployment tooling for AE team.
- Updates to the BigchainDB Server configuration settings: remove some settings (keys)
  and add some Tendermint-related settings. Some of this is done.
- More performance tests. Share how we do those tests. Share the results.
- More unit tests.
- Implement and begin using the network driver for tests.
- Four-node tests.
- More integration tests. For example, make more tests of `bigchaindb upsert-validator`.
- Increase code test coverage on the Events API.
- Run all tests on Travis CI, if possible.
- Implementation of [BEP-5/IDRP](https://github.com/bigchaindb/BEPs/pull/13)? What can we do now?
- A clean `bigchaindb` shutdown procedure. Generic process management.
- Crash-fault tolerance, e.g. Recover from MongoDB crashes into a consistent state. There has already been work on that.
- We'd like more production-ready ABCI server software. Support Tendermint 0.16. (We currently use `py-abci`; it needs more tests. Maybe use _different_ ABCI server software instead?)

## Assorted Other Things for the Near to Medium Term Future

- New way to compute the app hash based on the UTXO set, including an efficient way to update the Merkle tree used to compute the app hash from the UTXO set.
- No more 3scale (currently used by the BigchainDB Testnet)
- Support hashlock conditions (securely: need to make sure that every transaction is still signed by a client)
- Support timelock conditions
- (?) LevelDB vs other backends in Tendermint?
- A "secure" replacement for the `bigchaindb upsert-validator` subcommand.
- Plugins/extensions for specialized use cases
- Better logs
- Smart contract support. (Not necessarily within BigchainDB; maybe just better documentation about how to integrate with other smart-contract blockchains.)
- Prod-ready requirements of software that we use: Tendermint
- Refactoring
- Test what happens when a node runs out of memory or hard drive space.
  For example, what happens when there's no more space for MongoDB to write a block?
