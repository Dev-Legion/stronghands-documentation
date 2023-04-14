Queries
=========

This page provides some sample query examples to help get you started
with the Stronghands SHNDBar subgraph.

You can test any of the queries, or write your own, on the `Stronghands
SHNDBar
subgraph <https://thegraph.com/explorer/subgraph?id=9PNQKCFNijybeAXkfSYrrQQ9gtRhLJB8VgmBSov3RkDQ&view=Overview>`__.

Bar
---

This query returns the ID (contract address), decimal count and name of
the SHNDBar, as well as the contract address of SUSHI.

.. code:: graphql

   {
       bars(first: 5) {
           id
           decimals
           name
           sushi
       }
   }

User
----

This query grabs the first 15 users of the SHNDBar and returns the user
ID (user’s address), the SHNDBar address, the user’s total amount of
sSHND and how much (if any) sSHND they deposited.

.. code:: graphql

   {
       users(first: 5) {
           id
           bar {
               id
           }
           sSHND
           sSHNDIn
       }
   }
