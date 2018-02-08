# BigchainDB Roadmap

Below is a sketch of some of the things we plan to do in upcoming releases of BigchainDB Server (and associated software). It is, of course, subject to change.

The next release of BigchainDB Server has some significant changes and so the name of the software might change. The biggest change is from using MongoDB replication to using Tendermint replication. Most of the other changes are consequences of that one.

Not all changes between BigchainDB Server 1.3 and the next release are listed below. The "Next Release" list includes the main items to do as of 30 January, 2018.

## Next Release / Immediate Priorities

1. UTXO set / apphash for Tendermint + crash-fault tolerance
1. Prod-ready requirements of software that we use: py-abci
1. Shutdown procedure. (Generic process management.)
1. Ability to add validator nodes during runtime: allow less secure version for now.
1. "Scale up node": test what happens when a node runs out of memory.
1. Integration tests
1. Performance benchmarks
1. Setup a local node (i.e. standardize the process)
1. Finish HTTP API changes
1. BigchainDB configuration file updates
1. BigchainDB Server CLI updates (not the client-side CLI: deprecate that)
1. Also see [the Tendermint milestone](https://github.com/bigchaindb/bigchaindb/milestone/16) in GitHub.

## Next Priorities

- Three related items:
  1. Hashing transaction payloads (asset.data and metadata), to address legal issues
  1. Handle transactions & payloads
  1. (?) LevelDB vs other backends in Tendermint
- Ability to add validator nodes during runtime. The secure version (i.e. checking if enough of the existing node operators agree to it).
- No more 3scale (currently used by the BigchainDB Testnet)

## Assorted Other Things for the Future

- Plugins/extensions for specialized use cases
- Better queries / open MongoDB. For now, a node operator can allow full access to its local MongoDB instance by authenticated users: document that.
- Better logs
- Smart contract support. (Not necessarily within BigchainDB; maybe just better documentation about how to integrate with other smart-contract blockchains.)
- Prod-ready requirements of software that we use: Tendermint
- Refactoring
