# BigchainDB Roadmap

Below is a sketch of some of the things we plan to do in upcoming releases of BigchainDB Server (and associated software). It is, of course, subject to change.

The next release of BigchainDB Server has some significant changes and so the name of the software might change. The biggest change is from using MongoDB replication to using Tendermint replication. Most of the other changes are consequences of that one.

Not all changes between BigchainDB Server 1.3 and the next release are listed below. The "Next Release" list includes the main items to do as of 30 January, 2018.

## Next Release
## BigchainDB 2.0

The first BigchainDB 2.0 release will occur in March 2018. It will probably be named BigchainDB 2.0 Alpha. That release will be followed by Beta, RC1, RC2, etc., and then the final release, probably sometime in April 2018.

### Done for Sure

1. Finish HTTP API changes
1. Simplify & automate the production deployment process
1. Consolidate the proposal system (especially COSS)
1. Change the allowed transaction version number from "1.0" to "2.0"
1. Update the official drivers (Python driver & JavaScript driver)
1. BigchainDB Server CLI updates (not the client-side CLI: deprecate that)

### Not Done Yet, or Not Sure if Done Yet

1. Constructing the UTXO set and computing the app hash _the slow way_.
1. Prod-ready requirements of software that we use: py-abci
1. Shutdown procedure. (Generic process management.) Crash-fault tolerance.
   Recover from MongoDB crashes into a consistent state.
1. New `bigchaindb upsert-validator` subcommand to add/change/remove a validator at run time, "insecure" way. - PRs in review
1. Update and expand unit tests (single-node). Add four-node tests. Integration tests using network driver.
   Run all test on Travis CI, if possible.
1. Set up a network for the AE team to do some performance tests.
1. Standard process to set up a local node for development & testing, using Docker Compose
1. Update Ansible & Vagrant deployment tooling for AE team
1. BigchainDB Server configuration file updates: remove some settings (keys)
   and add some Tendermint-related settings
1. The Events API: update it and increase code coverage, with Tendermint included.

Also see [the Tendermint milestone](https://github.com/bigchaindb/bigchaindb/milestone/16) in GitHub.

## Next Priorities

- If you don't see your important must-have pet feature here, please see our docs on Contributing to BigchainDB (coming soon).
- Updating the UTXO set and computing the app hash _the efficient way_.
- Implementation of [5/IDRP](https://github.com/bigchaindb/BEPs/pull/13)? What can we do now?
- (?) LevelDB vs other backends in Tendermint?
- A "secure" replacement for the `bigchaindb upsert-validator` subcommand.
- No more 3scale (currently used by the BigchainDB Testnet)
- Performance benchmarks

## Assorted Other Things for the Future

- Plugins/extensions for specialized use cases
- Better queries / open MongoDB. For now, a node operator can allow full access to its local MongoDB instance by authenticated users: document that.
- Better logs
- Smart contract support. (Not necessarily within BigchainDB; maybe just better documentation about how to integrate with other smart-contract blockchains.)
- Prod-ready requirements of software that we use: Tendermint
- Refactoring
- Test what happens when a node runs out of memory or hard drive space.
  For example, what happens when there's no more space for MongoDB to write a block?
