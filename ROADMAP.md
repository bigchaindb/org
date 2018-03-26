# BigchainDB Roadmap

Below is a sketch of some of the things we plan to do in upcoming releases of BigchainDB Server (and associated software). It is, of course, subject to change.

BigchainDB 2.0 has several changes. The biggest is the switch from using MongoDB for replication and consensus to using Tendermint for that. Most of the other changes are consequences of that one.

Not all changes between BigchainDB Server 1.3 and 2.0 are listed below. The "Next Release" list includes the main items to do as of 30 January, 2018.

## Next Release
## BigchainDB 2.0

The first BigchainDB 2.0 release will occur in March 2018. It will probably be named BigchainDB 2.0 Alpha. That release will be followed by Beta, RC1, RC2, etc., and then the final release, BigchainDB 2.0, probably sometime in April 2018.

### Done for Sure

1. Finish HTTP API changes
1. Simplify & automate the production deployment process
1. Consolidate the proposal system (especially COSS)
1. Change the allowed transaction version number from "1.0" to "2.0"
1. Update the official drivers (Python driver & JavaScript driver)
1. BigchainDB Server CLI updates (not the client-side CLI: deprecate that)
1. Compute an app hash for Tendermint (in a dumb way _that works_).
1. Standard process to set up a local node for development & testing, using Docker Compose.

### Not Done Yet, or Not Sure if Done Yet

1. New `bigchaindb upsert-validator` subcommand to add/change/remove a validator at run time, "insecure" way. - PRs in review
1. Update and expand unit tests (single-node). Add four-node tests. Integration tests using network driver.
   Run all test on Travis CI, if possible.
1. Set up a network for the AE team to do some performance tests. Coming soon!
1. Update Ansible & Vagrant deployment tooling for AE team. Coming soon!
1. BigchainDB Server configuration file updates: remove some settings (keys)
   and add some Tendermint-related settings. Some of this is done...
1. The Events API: update it and increase code coverage, with Tendermint included.
1. Better queries / open MongoDB. A node operator can allow full access to its
   local MongoDB instance by authenticated users: document that.

Also see [the Tendermint milestone](https://github.com/bigchaindb/bigchaindb/milestone/16) in GitHub.

## Next Priorities

- If you don't see your important must-have pet feature here, please see our docs on Contributing to BigchainDB (coming soon).
- More integration tests.
- Efficiently updating the UTXO Set and computing the app hash with each new block.
- Implementation of [BEP-5/IDRP](https://github.com/bigchaindb/BEPs/pull/13)? What can we do now?
- (?) LevelDB vs other backends in Tendermint?
- A "secure" replacement for the `bigchaindb upsert-validator` subcommand.
- A clean `bigchaindb` shutdown procedure. Generic process management.
- Crash-fault tolerance, e.g. Recover from MongoDB crashes into a consistent state.
- Improve the production-readiness of the ABCI software we use. Currently that is `py-abci`; it needs more tests. Maybe use _different_ ABCI server software instead (e.g. one that is already better-tested)?
- No more 3scale (currently used by the BigchainDB Testnet)
- Performance benchmarks

## Assorted Other Things for the Future

- Plugins/extensions for specialized use cases
- Better logs
- Smart contract support. (Not necessarily within BigchainDB; maybe just better documentation about how to integrate with other smart-contract blockchains.)
- Prod-ready requirements of software that we use: Tendermint
- Refactoring
- Test what happens when a node runs out of memory or hard drive space.
  For example, what happens when there's no more space for MongoDB to write a block?
