# BigchainDB Roadmap

Below is a sketch of some of the things we plan to do in upcoming releases of BigchainDB Server (and associated software). It is, of course, subject to change.

BigchainDB 2.0 has several changes. The biggest is the switch from using MongoDB for replication and consensus to using Tendermint for that. Most of the other changes are consequences of that one. Not all changes between BigchainDB Server 1.3 and 2.0 are listed below. The "Next Release" list includes the main items to do as of 30 January, 2018.

## Next Release: BigchainDB 2.0 Alpha

The BigchainDB 2.0 Alpha release will occur in March 2018. That release will be followed by Beta, RC1, RC2, etc., and then the final release, BigchainDB 2.0, probably sometime in April 2018.

### Done for Sure

1. Finish HTTP API changes
1. Simplify & automate the production deployment process
1. Consolidate the proposal system (especially COSS)
1. Change the allowed transaction version number from "1.0" to "2.0"
1. Update the official drivers (Python driver & JavaScript driver)
1. BigchainDB Server CLI updates (not the client-side CLI: deprecate that)
1. Compute an app hash for Tendermint (in a dumb way _that works_).
1. Standard process to set up a local node for development & testing, using Docker Compose.
1. Set up a network for the AE team to do some performance tests.

### Not Done Yet, or Not Sure if Done Yet

1. New `bigchaindb upsert-validator` subcommand to add/change/remove a validator at run time, "insecure" way. - All remaining open PRs are ready to merge.
1. Update Ansible & Vagrant deployment tooling for AE team. Coming soon!
1. BigchainDB Server configuration file updates: remove some settings (keys)
   and add some Tendermint-related settings. Some of this is done...
1. The Events API: update it and increase code coverage, with Tendermint included.

We have a [kanban board (GitHub organization project board) to track the status of BigchainDB 2.0 tasks](https://github.com/orgs/bigchaindb/projects/4). To view it, you must be a member of the **bigchaindb** organization on GitHub; you can ask to be added by emailing troy@bigchaindb.com. In the future, we might use a third-party tool to publish the content of that board on a public website. (GitHub won't let us make the board public. That's not an option.)

## Next Priorities

- If you don't see your important feature here, please read about how to request a feature in our docs on [Contributing to BigchainDB](https://docs.bigchaindb.com/projects/contributing/en/latest/index.html).
- Write about how a node operator can expose the full power of MongoDB to users. For example, they could allow users to make any valid MongoDB query.
- More performance tests. Share how we do those tests. Share the results.
- More unit tests.
- Implement and begin using the network driver for tests.
- Four-node tests.
- More integration tests. For example, make more tests of `bigchaindb upsert-validator`.
- Run all test on Travis CI, if possible.
- Efficiently update the UTXO Set and compute the app hash with each new block.
- Implementation of [BEP-5/IDRP](https://github.com/bigchaindb/BEPs/pull/13)? What can we do now?
- A clean `bigchaindb` shutdown procedure. Generic process management.
- Crash-fault tolerance, e.g. Recover from MongoDB crashes into a consistent state. There has already been work on that.
- We'd like more production-ready ABCI server software. (We currently use `py-abci`; it needs more tests. Maybe use _different_ ABCI server software instead?)
- No more 3scale (currently used by the BigchainDB Testnet)

## Assorted Other Things for the Future

- (?) LevelDB vs other backends in Tendermint?
- A "secure" replacement for the `bigchaindb upsert-validator` subcommand.
- Plugins/extensions for specialized use cases
- Better logs
- Smart contract support. (Not necessarily within BigchainDB; maybe just better documentation about how to integrate with other smart-contract blockchains.)
- Prod-ready requirements of software that we use: Tendermint
- Refactoring
- Test what happens when a node runs out of memory or hard drive space.
  For example, what happens when there's no more space for MongoDB to write a block?
