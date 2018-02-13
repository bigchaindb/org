# BigchainDB Roadmap

Below is a sketch of some of the things we plan to do in upcoming releases of BigchainDB Server (and associated software). It is, of course, subject to change.

The next release of BigchainDB Server has some significant changes and so the name of the software might change. The biggest change is from using MongoDB replication to using Tendermint replication. Most of the other changes are consequences of that one.

Not all changes between BigchainDB Server 1.3 and the next release are listed below. The "Next Release" list includes the main items to do as of 30 January, 2018.

## Next Release / Immediate Priorities

1. UTXO set / apphash for Tendermint
1. Prod-ready requirements of software that we use: py-abci
1. Shutdown procedure. (Generic process management.) Crash-fault tolerance.
   Recover from MongoDB crashes into a consistent state.
1. Ability to add validator nodes during runtime: allow a less-secure version for now.
1. Update and expand unit tests (single-node). Add four-node tests. Integration tests using network driver.
   Run all test on Travis CI, if possible.
1. Set up a network for the AE team to do some performance tests.
1. Standard process to set up a local node for development & testing, using Docker Compose
1. Update Ansible & Vagrant deployment tooling for AE team
1. Simplify & automate the production deployment process
1. Finish HTTP API changes
1. BigchainDB Server configuration file updates: remove some settings (keys)
   and add some Tendermint-related settings
1. BigchainDB Server CLI updates (not the client-side CLI: deprecate that)
1. Consolidate the proposal system (especially COSS)
1. Increase code coverage of the event stream API, with Tendermint included.
1. Change the allowed transaction version number from "1.0" to "2.0"
1. Update the official drivers (Python driver & JavaScript driver)

Also see [the Tendermint milestone](https://github.com/bigchaindb/bigchaindb/milestone/16) in GitHub.

## Next Priorities

- Three related items:
  1. Hashing transaction payloads (asset.data and metadata), to address legal issues
  1. Handle transactions & payloads
  1. (?) LevelDB vs other backends in Tendermint
- Ability to add validator nodes during runtime. The secure version (i.e. checking if enough of the existing node operators agree to it).
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
