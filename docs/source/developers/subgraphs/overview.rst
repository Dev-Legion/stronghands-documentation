Overview
========

The following pages contain everything you need to know about the Stronghands suite of subgraphs. Stronghands subgraphs are powered by The Graph <https://thegraph.com/en/>__, a protocol for building decentralized applications (dApps) quickly on Ethereum and IPFS using GraphQL.

If you are unfamiliar with GraphQL, we recommend taking a quick look through their documentation first here <https://graphql.org/learn/>__.

The Stronghands subgraph works by listening for events emitted by one or more data sources (Smart Contracts) on the various chains. It handles the indexing and caching of data which can later be queried using an exposed GraphQL API, providing an excellent developer experience.

Each subgraph is broken down into its own section and documented in two forms: by entity and by queries.

Current Subgraph Locations

Exchange
^^^^^^^^

Includes all Stronghands Exchange data with Price Data, Volume, Users, etc.

`Binance <https://thegraph.com/explorer/subgraph/sushiswap/bsc-exchange>`_

ShndMaker
^^^^^^^^^

Indexes the ShndMaker contract, which handles the serving of exchange fees to the SHNDBar.

`Binance <https://thegraph.com/explorer/subgraph/sushiswap/sushi-maker>`_

SHNDBar
^^^^^^^

Indexes the SHNDBar, which includes all the data related to the bar.

`Binance <https://thegraph.com/explorer/subgraph/sushiswap/sushi-bar>`_

Resources
`Stronghands Subgraph Explorer <https://thegraph.com/hosted-service/subgraph/sushiswap/exchange>`_
`Stronghands Subgraph Source Code <https://github.com/sushiswap/sushiswap-subgraph>`_
`The Graph <https://thegraph.com/docs/en/>`_
`GraphQL <https://graphql.org/learn/>`_