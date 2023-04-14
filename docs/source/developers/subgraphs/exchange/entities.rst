Entities
=========

Entities for the Exchange subgraph are all listed below.

Factory
~~~~~~~

+-------------+------+-------------------------------------------------+
| Field       | Type | Description                                     |
+=============+======+=================================================+
| ``id``      | ID   | factory address                                 |
+-------------+------+-------------------------------------------------+
| ``          | Bi   | all time volume across pairs stored as a        |
| volumeUSD`` | gDec | derived amount of USD                           |
|             | imal |                                                 |
+-------------+------+-------------------------------------------------+
| ``          | Bi   | all time volume across pairs stored as a        |
| volumeETH`` | gDec | derived amount of ETH                           |
|             | imal |                                                 |
+-------------+------+-------------------------------------------------+
| ``untracked | Bi   | all time untracked volume across pairs stored   |
| VolumeUSD`` | gDec | as a derived amount of USD                      |
|             | imal |                                                 |
+-------------+------+-------------------------------------------------+
| ``liq       | Bi   | all time liquidity across pairs stored as a     |
| uidityUSD`` | gDec | derived amount of USD                           |
|             | imal |                                                 |
+-------------+------+-------------------------------------------------+
| ``liq       | Bi   | all time liquidity across pairs stored as a     |
| uidityETH`` | gDec | derived amount of ETH                           |
|             | imal |                                                 |
+-------------+------+-------------------------------------------------+
| ``txCount`` | Bi   | all time transaction count                      |
|             | gInt |                                                 |
+-------------+------+-------------------------------------------------+
| ``t         | Bi   | token count                                     |
| okenCount`` | gInt |                                                 |
+-------------+------+-------------------------------------------------+
| ``          | Bi   | pair count                                      |
| pairCount`` | gInt |                                                 |
+-------------+------+-------------------------------------------------+
| ``          | Bi   | user count                                      |
| userCount`` | gInt |                                                 |
+-------------+------+-------------------------------------------------+
| ``pairs``   | [Pa  | array of pair ids                               |
|             | irs] |                                                 |
+-------------+------+-------------------------------------------------+
| ``tokens``  | `T   | array of tokens                                 |
|             | oken |                                                 |
|             |  <#t |                                                 |
|             | oken |                                                 |
|             | >`__ |                                                 |
+-------------+------+-------------------------------------------------+
| `           | `Hou | array of hour data                              |
| `hourData`` | rDat |                                                 |
|             | a <# |                                                 |
|             | hour |                                                 |
|             | data |                                                 |
|             | >`__ |                                                 |
+-------------+------+-------------------------------------------------+
| ``dayData`` | `D   | array of day data                               |
|             | ayDa |                                                 |
|             | ta < |                                                 |
|             | #day |                                                 |
|             | data |                                                 |
|             | >`__ |                                                 |
+-------------+------+-------------------------------------------------+

Token
~~~~~

+-----------------------+-----------------------+-----------------------+
| Field                 | Type                  | Description           |
+=======================+=======================+=======================+
| ``id``                | ID                    | token address         |
+-----------------------+-----------------------+-----------------------+
| ``factory``           | Factory               | factory               |
+-----------------------+-----------------------+-----------------------+
| ``symbol``            | String                | token symbol          |
+-----------------------+-----------------------+-----------------------+
| ``name``              | String                | token name            |
+-----------------------+-----------------------+-----------------------+
| ``decimals``          | BigInt                | token decimals        |
+-----------------------+-----------------------+-----------------------+
| ``totalSupply``       | BigInt                | total supply of token |
+-----------------------+-----------------------+-----------------------+
| ``volume``            | BigDecimal            | amount of token       |
|                       |                       | traded all time       |
|                       |                       | across all pairs      |
+-----------------------+-----------------------+-----------------------+
| ``volumeUSD``         | BigDecimal            | amount of token       |
|                       |                       | traded all time       |
|                       |                       | across all pairs      |
|                       |                       | stored as a derived   |
|                       |                       | amount of USD         |
+-----------------------+-----------------------+-----------------------+
| `                     | BigDecimal            | all time untracked    |
| `untrackedVolumeUSD`` |                       | volume across all     |
|                       |                       | pairs stored as a     |
|                       |                       | derived amount of USD |
+-----------------------+-----------------------+-----------------------+
| ``txCount``           | BigInt                | all time transaction  |
|                       |                       | count of token across |
|                       |                       | all pairs             |
+-----------------------+-----------------------+-----------------------+
| ``liquidity``         | BigDecimal            | amount of token       |
|                       |                       | provided as liquidity |
|                       |                       | across all pairs      |
+-----------------------+-----------------------+-----------------------+
| ``derivedETH``        | BigDecimal            | ETH per token         |
+-----------------------+-----------------------+-----------------------+
| ``whitelistPairs``    | `Pair <#pair>`__      | array of whitelisted  |
|                       |                       | pairs                 |
+-----------------------+-----------------------+-----------------------+
| ``hourData``          | `TokenHourDat         | array of token hour   |
|                       | a <#tokenhourdata>`__ | data                  |
+-----------------------+-----------------------+-----------------------+
| ``dayData``           | `TokenDayDa           | array of token day    |
|                       | ta <#tokendaydata>`__ | data                  |
+-----------------------+-----------------------+-----------------------+
| ``basePairs``         | `Pair <#pair>`__      | array of base pairs   |
+-----------------------+-----------------------+-----------------------+
| ``quotePairs``        | `Pair <#pair>`__      | array of quote pairs  |
+-----------------------+-----------------------+-----------------------+
| ``basePairsDayData``  | `PairDayD             | array of hour data    |
|                       | ata <#pairdaydata>`__ |                       |
+-----------------------+-----------------------+-----------------------+
| ``quotePairsDayData`` | `PairDayD             | array of day data     |
|                       | ata <#pairdaydata>`__ |                       |
+-----------------------+-----------------------+-----------------------+

Pair
~~~~

+-----------------------+-----------------------+-----------------------+
| Field                 | Type                  | Description           |
+=======================+=======================+=======================+
| ``id``                | ID                    | pair address          |
+-----------------------+-----------------------+-----------------------+
| ``factory``           | Factory               | factory               |
+-----------------------+-----------------------+-----------------------+
| ``name``              | String                | pair name             |
+-----------------------+-----------------------+-----------------------+
| ``token0``            | Token                 | reference to token0   |
|                       |                       | stored in pair        |
|                       |                       | contract              |
+-----------------------+-----------------------+-----------------------+
| ``token1``            | Token                 | reference to token1   |
|                       |                       | stored in pair        |
|                       |                       | contract              |
+-----------------------+-----------------------+-----------------------+
| ``reserve0``          | BigDecimal            | reserve of token0     |
+-----------------------+-----------------------+-----------------------+
| ``reserve1``          | BigDecimal            | reserve of token1     |
+-----------------------+-----------------------+-----------------------+
| ``totalSupply``       | BigDecimal            | total supply of       |
|                       |                       | liquidity token       |
|                       |                       | distributed to        |
|                       |                       | liquidity providers   |
+-----------------------+-----------------------+-----------------------+
| ``reserveETH``        | BigDecimal            | total liquidity in    |
|                       |                       | pair stored as amount |
|                       |                       | of ETH                |
+-----------------------+-----------------------+-----------------------+
| ``reserveUSD``        | BigDecimal            | total liquidity in    |
|                       |                       | pair stored as amount |
|                       |                       | of USD                |
+-----------------------+-----------------------+-----------------------+
| ``trackedReserveETH`` | BigDecimal            | used for separating   |
|                       |                       | per pair reserves and |
|                       |                       | global                |
+-----------------------+-----------------------+-----------------------+
| ``token0Price``       | BigDecimal            | token0 per token1     |
+-----------------------+-----------------------+-----------------------+
| ``token1Price``       | BigDecimal            | token1 per token0     |
+-----------------------+-----------------------+-----------------------+
| ``volumeToken0``      | BigDecimal            | amount of token0      |
|                       |                       | swapped on this pair  |
+-----------------------+-----------------------+-----------------------+
| ``volumeToken1``      | BigDecimal            | amount of token1      |
|                       |                       | swapped on this pair  |
+-----------------------+-----------------------+-----------------------+
| ``volumeUSD``         | BigDecimal            | all time volume on    |
|                       |                       | this pair stored as a |
|                       |                       | derived amount of USD |
+-----------------------+-----------------------+-----------------------+
| `                     | BigDecimal            | all time untracked    |
| `untrackedVolumeUSD`` |                       | volume on this pair   |
|                       |                       | stored as a derived   |
|                       |                       | amount of USD         |
+-----------------------+-----------------------+-----------------------+
| ``txCount``           | BigInt                | all time transaction  |
|                       |                       | count on this pair    |
+-----------------------+-----------------------+-----------------------+
| ``liq                 | BigInt                | liquidity provider    |
| uidityProviderCount`` |                       | count for this pair   |
+-----------------------+-----------------------+-----------------------+
| `                     | `LiquidityPosition <# | array of liquidity    |
| `liquidityPositions`` | liquidityposition>`__ | positions             |
+-----------------------+-----------------------+-----------------------+
| ``liquidi             | [Liquid               | array of snapshots    |
| tyPositionSnapshots`` | ityProvisionSnapshot] |                       |
+-----------------------+-----------------------+-----------------------+
| ``dayData``           | `PairDayD             | pair day data         |
|                       | ata <#pairdaydata>`__ |                       |
+-----------------------+-----------------------+-----------------------+
| ``hourData``          | [PairHourData]        | pair hour data        |
+-----------------------+-----------------------+-----------------------+
| ``mints``             | `Mint <#mint>`__      | array of mints for    |
|                       |                       | pair                  |
+-----------------------+-----------------------+-----------------------+
| ``burns``             | `Burn <#burn>`__      | array of burns for    |
|                       |                       | pair                  |
+-----------------------+-----------------------+-----------------------+
| ``swaps``             | `Swap <#swap>`__      | array of swaps for    |
|                       |                       | pair                  |
+-----------------------+-----------------------+-----------------------+
| ``timestamp``         | BigInt                | timestamp             |
+-----------------------+-----------------------+-----------------------+
| ``block``             | BigInt                | block contract was    |
|                       |                       | created at            |
+-----------------------+-----------------------+-----------------------+

User
~~~~

A user entity is created for any unknown address that provides liquidity
to a pool on SushiSwap. It can be used to track active liquidity
positions and all time value in USD of swaps performed by the user.

+------------------+-----------------+---------------------------------+
| Field            | Type            | Description                     |
+==================+=================+=================================+
| ``id``           | ID              | user address                    |
+------------------+-----------------+---------------------------------+
| ``liqu           | `LiquidityPo    | array of active liquidity       |
| idityPositions`` | sition <#liquid | positions                       |
|                  | ityposition>`__ |                                 |
+------------------+-----------------+---------------------------------+

LiquidityPosition
~~~~~~~~~~~~~~~~~

+------------------+---------------------+-----------------------------+
| Field            | Type                | Description                 |
+==================+=====================+=============================+
| ``id``           | ID                  | pair address                |
+------------------+---------------------+-----------------------------+
| ``user``         | User                | user reference              |
+------------------+---------------------+-----------------------------+
| ``pair``         | Pair                | pair reference              |
+------------------+---------------------+-----------------------------+
| ``liquidi        | BigDecimal          | amount of liquidity token   |
| tyTokenBalance`` |                     |                             |
+------------------+---------------------+-----------------------------+
| ``snapshots``    | `                   | array of liquidity position |
|                  | LiquidityPositionSn | snapshots                   |
|                  | apshot <#liquidityp |                             |
|                  | ositionsnapshot>`__ |                             |
+------------------+---------------------+-----------------------------+
| ``block``        | Int                 | block                       |
+------------------+---------------------+-----------------------------+
| ``timestamp``    | Int                 | timestamp                   |
+------------------+---------------------+-----------------------------+

LiquidityPositionSnapshot
~~~~~~~~~~~~~~~~~~~~~~~~~

+---------------------+-------------+---------------------------------+
| Field               | Type        | Description                     |
+=====================+=============+=================================+
| ``id``              | ID          | id                              |
+---------------------+-------------+---------------------------------+
| ``                  | Liquid      | liquidity position              |
| liquidityPosition`` | ityPosition |                                 |
+---------------------+-------------+---------------------------------+
| ``timestamp``       | Int         | timestamp for quick historical  |
|                     |             | lookups                         |
+---------------------+-------------+---------------------------------+
| ``block``           | Int         | block number for quick          |
|                     |             | historical lookups              |
+---------------------+-------------+---------------------------------+
| ``user``            | User        | user                            |
+---------------------+-------------+---------------------------------+
| ``pair``            | Pair        | pair                            |
+---------------------+-------------+---------------------------------+
| ``token0PriceUSD``  | BigDecimal  | token0 price in USD             |
+---------------------+-------------+---------------------------------+
| ``token1PriceUSD``  | BigDecimal  | token1 price in USD             |
+---------------------+-------------+---------------------------------+
| ``reserve0``        | BigDecimal  | snapshot of pair token0         |
|                     |             | reserves                        |
+---------------------+-------------+---------------------------------+
| ``reserve1``        | BigDecimal  | snapshot of pair token1         |
|                     |             | reserves                        |
+---------------------+-------------+---------------------------------+
| ``reserveUSD``      | BigDecimal  | snapshot of pair reserves in    |
|                     |             | USD                             |
+---------------------+-------------+---------------------------------+
| ``liquidit          | BigDecimal  | snapshot of pool’s token supply |
| yTokenTotalSupply`` |             |                                 |
+---------------------+-------------+---------------------------------+
| ``liqu              | BigDecimal  | snapshot of user’s pool token   |
| idityTokenBalance`` |             | balance                         |
+---------------------+-------------+---------------------------------+

Transaction
~~~~~~~~~~~

=============== ================ =================================
Field           Type             Description
=============== ================ =================================
``id``          ID               transaction hash
``blockNumber`` BigInt           block transaction was mined
``timestamp``   BigInt           timestamp transaction was created
``mints``       `Mint <#mint>`__ array of Mint events
``burns``       `Burn <#burn>`__ array of Burn events
``swaps``       `Swap <#swap>`__ array of Swap events
=============== ================ =================================

Mint
~~~~

+--------+------+------------------------------------------------------+
| Field  | Type | Description                                          |
+========+======+======================================================+
| ``id`` | ID   | transaction hash, a hyphen and the index in the      |
|        |      | transaction mint array, concatenated                 |
+--------+------+------------------------------------------------------+
| ``t    | Tra  | reference to transaction                             |
| ransac | nsac |                                                      |
| tion`` | tion |                                                      |
+--------+------+------------------------------------------------------+
| `      | Bi   | timestamp mint was created                           |
| `times | gInt |                                                      |
| tamp`` |      |                                                      |
+--------+------+------------------------------------------------------+
| ``     | Pair | reference to pair                                    |
| pair`` |      |                                                      |
+--------+------+------------------------------------------------------+
| ``to`` | B    | address of recipient                                 |
|        | ytes |                                                      |
+--------+------+------------------------------------------------------+
| `      | Bi   | amount of liquidity tokens minted                    |
| `liqui | gDec |                                                      |
| dity`` | imal |                                                      |
+--------+------+------------------------------------------------------+
| ``se   | B    | address of initiator                                 |
| nder`` | ytes |                                                      |
+--------+------+------------------------------------------------------+
| ``amo  | Bi   | amount of token0                                     |
| unt0`` | gDec |                                                      |
|        | imal |                                                      |
+--------+------+------------------------------------------------------+
| ``amo  | Bi   | amount of token1                                     |
| unt1`` | gDec |                                                      |
|        | imal |                                                      |
+--------+------+------------------------------------------------------+
| ``logI | Bi   | index in the transaction event that was emitted      |
| ndex`` | gInt |                                                      |
+--------+------+------------------------------------------------------+
| `      | Bi   | value of token0 and token1 in USD                    |
| `amoun | gDec |                                                      |
| tUSD`` | imal |                                                      |
+--------+------+------------------------------------------------------+
| ``f    | B    | address of fee recipient                             |
| eeTo`` | ytes |                                                      |
+--------+------+------------------------------------------------------+
| ``fe   | Bi   | amount of liquidity sent to fee recipient            |
| eLiqui | gDec |                                                      |
| dity`` | imal |                                                      |
+--------+------+------------------------------------------------------+

Burn
~~~~

+--------+------+------------------------------------------------------+
| Field  | Type | Description                                          |
+========+======+======================================================+
| ``id`` | ID   | transaction hash, a hyphen and the index in the      |
|        |      | transaction burn array, concatenated                 |
+--------+------+------------------------------------------------------+
| ``t    | Tra  | reference to transaction                             |
| ransac | nsac |                                                      |
| tion`` | tion |                                                      |
+--------+------+------------------------------------------------------+
| `      | Bi   | timestamp burn was created                           |
| `times | gInt |                                                      |
| tamp`` |      |                                                      |
+--------+------+------------------------------------------------------+
| ``     | Pair | reference to pair                                    |
| pair`` |      |                                                      |
+--------+------+------------------------------------------------------+
| ``to`` | B    | address of recipient                                 |
|        | ytes |                                                      |
+--------+------+------------------------------------------------------+
| `      | Bi   | amount of liquidity tokens burned                    |
| `liqui | gDec |                                                      |
| dity`` | imal |                                                      |
+--------+------+------------------------------------------------------+
| ``se   | B    | address of initiator                                 |
| nder`` | ytes |                                                      |
+--------+------+------------------------------------------------------+
| ``amo  | Bi   | amount of token0 burned                              |
| unt0`` | gDec |                                                      |
|        | imal |                                                      |
+--------+------+------------------------------------------------------+
| ``amo  | Bi   | amount of token1 burned                              |
| unt1`` | gDec |                                                      |
|        | imal |                                                      |
+--------+------+------------------------------------------------------+
| ``logI | Bi   | index in the transaction event that was emitted      |
| ndex`` | gInt |                                                      |
+--------+------+------------------------------------------------------+
| `      | Bi   | value of token0 and token1 in USD                    |
| `amoun | gDec |                                                      |
| tUSD`` | imal |                                                      |
+--------+------+------------------------------------------------------+
| ``comp | Boo  | false in ETH case                                    |
| lete`` | lean |                                                      |
+--------+------+------------------------------------------------------+
| ``f    | B    | address of fee recipient                             |
| eeTo`` | ytes |                                                      |
+--------+------+------------------------------------------------------+
| ``fe   | Bi   | amount of liquidity sent to fee recipient            |
| eLiqui | gDec |                                                      |
| dity`` | imal |                                                      |
+--------+------+------------------------------------------------------+

Swap
~~~~

+-------+------+-------------------------------------------------------+
| Field | Type | Description                                           |
+=======+======+=======================================================+
| `     | ID   | transaction hash, a hyphen and the index in the       |
| `id`` |      | transaction burn array, concatenated                  |
+-------+------+-------------------------------------------------------+
| ``tra | Tra  | reference to transaction                              |
| nsact | nsac |                                                       |
| ion`` | tion |                                                       |
+-------+------+-------------------------------------------------------+
| ``t   | Bi   | timestamp swap was created                            |
| imest | gInt |                                                       |
| amp`` |      |                                                       |
+-------+------+-------------------------------------------------------+
| ``p   | Pair | reference to pair                                     |
| air`` |      |                                                       |
+-------+------+-------------------------------------------------------+
| ``sen | B    | address of initiator                                  |
| der`` | ytes |                                                       |
+-------+------+-------------------------------------------------------+
| ``a   | Bi   | amount of token0 to swap                              |
| mount | gDec |                                                       |
| 0In`` | imal |                                                       |
+-------+------+-------------------------------------------------------+
| ``a   | Bi   | amount of token1 to swap                              |
| mount | gDec |                                                       |
| 1In`` | imal |                                                       |
+-------+------+-------------------------------------------------------+
| ``am  | Bi   | amount of token0 received                             |
| ount0 | gDec |                                                       |
| Out`` | imal |                                                       |
+-------+------+-------------------------------------------------------+
| ``am  | Bi   | amount of token1 received                             |
| ount1 | gDec |                                                       |
| Out`` | imal |                                                       |
+-------+------+-------------------------------------------------------+
| `     | B    | address of recipient                                  |
| `to`` | ytes |                                                       |
+-------+------+-------------------------------------------------------+
| ``    | Bi   | index in the transaction event that was emitted       |
| logIn | gInt |                                                       |
| dex`` |      |                                                       |
+-------+------+-------------------------------------------------------+
| ``a   | Bi   | value of token0 and token1 in USD                     |
| mount | gDec |                                                       |
| USD`` | imal |                                                       |
+-------+------+-------------------------------------------------------+

Bundle
~~~~~~

+-----+-----+---------------------------------------------------------+
| Fi  | T   | Description                                             |
| eld | ype |                                                         |
+=====+=====+=========================================================+
| ``i | ID  | transaction hash, a hyphen and the index in the         |
| d`` |     | transaction burn array, concatenated                    |
+-----+-----+---------------------------------------------------------+
| ``e | B   | price of ETH in USD                                     |
| thP | igD |                                                         |
| ric | eci |                                                         |
| e`` | mal |                                                         |
+-----+-----+---------------------------------------------------------+

DayData
~~~~~~~

Combined pair data aggregated daily.

+------------+------+--------------------------------------------------+
| Field      | Type | Description                                      |
+============+======+==================================================+
| ``id``     | ID   | unix timestamp for the start of the day / 86400  |
+------------+------+--------------------------------------------------+
| `          | Fac  | factory                                          |
| `factory`` | tory |                                                  |
+------------+------+--------------------------------------------------+
| ``date``   | Int  | unix timestamp for the start of the day          |
+------------+------+--------------------------------------------------+
| ``v        | Bi   | volume across all pairs stored as a derived      |
| olumeETH`` | gDec | amount of ETH                                    |
|            | imal |                                                  |
+------------+------+--------------------------------------------------+
| ``v        | Bi   | volume across all pairs stored as a derived      |
| olumeUSD`` | gDec | amount of USD                                    |
|            | imal |                                                  |
+------------+------+--------------------------------------------------+
| ``untrack  | Bi   | untracked volume across all pairs                |
| edVolume`` | gDec |                                                  |
|            | imal |                                                  |
+------------+------+--------------------------------------------------+
| ``liqu     | Bi   | total liquidity across all pairs stored as a     |
| idityETH`` | gDec | derived amount of ETH                            |
|            | imal |                                                  |
+------------+------+--------------------------------------------------+
| ``liqu     | Bi   | total liquidity across all pairs stored as a     |
| idityUSD`` | gDec | derived amount of USD                            |
|            | imal |                                                  |
+------------+------+--------------------------------------------------+
| `          | Bi   | total number of transactions                     |
| `txCount`` | gInt |                                                  |
+------------+------+--------------------------------------------------+

HourData
~~~~~~~~

+------------+------+--------------------------------------------------+
| Field      | Type | Description                                      |
+============+======+==================================================+
| ``id``     | ID   | unix timestamp for the start of hour             |
+------------+------+--------------------------------------------------+
| `          | Fac  | factory                                          |
| `factory`` | tory |                                                  |
+------------+------+--------------------------------------------------+
| ``date``   | Int  | unix timestamp for the start of the day          |
+------------+------+--------------------------------------------------+
| ``v        | Bi   | volume across all pairs stored as a derived      |
| olumeETH`` | gDec | amount of ETH                                    |
|            | imal |                                                  |
+------------+------+--------------------------------------------------+
| ``v        | Bi   | volume across all pairs stored as a derived      |
| olumeUSD`` | gDec | amount of USD                                    |
|            | imal |                                                  |
+------------+------+--------------------------------------------------+
| ``untrack  | Bi   | untracked volume across all pairs                |
| edVolume`` | gDec |                                                  |
|            | imal |                                                  |
+------------+------+--------------------------------------------------+
| ``liqu     | Bi   | total liquidity across all pairs stored as a     |
| idityETH`` | gDec | derived amount of ETH                            |
|            | imal |                                                  |
+------------+------+--------------------------------------------------+
| ``liqu     | Bi   | total liquidity across all pairs stored as a     |
| idityUSD`` | gDec | derived amount of USD                            |
|            | imal |                                                  |
+------------+------+--------------------------------------------------+
| `          | Bi   | total number of transactions                     |
| `txCount`` | gInt |                                                  |
+------------+------+--------------------------------------------------+

PairDayData
~~~~~~~~~~~

Pair data aggreated daily.

+-----------------------+-----------------------+-----------------------+
| Field                 | Type                  | Description           |
+=======================+=======================+=======================+
| ``id``                | ID                    | pair address          |
|                       |                       | concatenated with day |
|                       |                       | id (unix timestamp    |
|                       |                       | for the start of the  |
|                       |                       | day / 86400)          |
+-----------------------+-----------------------+-----------------------+
| ``date``              | Int                   | unix timestamp for    |
|                       |                       | the start of the day  |
+-----------------------+-----------------------+-----------------------+
| ``pairAddress``       | Bytes                 | pair address          |
+-----------------------+-----------------------+-----------------------+
| ``token0``            | Token                 | token0 reference      |
+-----------------------+-----------------------+-----------------------+
| ``token1``            | Token                 | token1 reference      |
+-----------------------+-----------------------+-----------------------+
| ``reserveUSD``        | BigDecimal            | reserve of token0 and |
|                       |                       | token1 as the derived |
|                       |                       | amount of USD         |
+-----------------------+-----------------------+-----------------------+
| ``volumeToken0``      | BigDecimal            | amount of token0      |
|                       |                       | swapped               |
+-----------------------+-----------------------+-----------------------+
| ``volumeToken1``      | BigDecimal            | amount of token1      |
|                       |                       | swapped               |
+-----------------------+-----------------------+-----------------------+
| ``volumeUSD``         | BigDecimal            | volume of pairs as    |
|                       |                       | the derived amount of |
|                       |                       | USD                   |
+-----------------------+-----------------------+-----------------------+
| ``txCount``           | BigInt                | amount of             |
|                       |                       | transactions on pair  |
+-----------------------+-----------------------+-----------------------+

TokenDayData
~~~~~~~~~~~~

Token data across related pairs aggregated daily.

+-----------------------+-----------------------+-----------------------+
| Field                 | Type                  | Description           |
+=======================+=======================+=======================+
| ``id``                | ID                    | pair address          |
|                       |                       | concatenated with day |
|                       |                       | id (unix timestamp    |
|                       |                       | for the start of the  |
|                       |                       | day / 86400)          |
+-----------------------+-----------------------+-----------------------+
| ``date``              | Int                   | unix timestamp for    |
|                       |                       | the start of the day  |
+-----------------------+-----------------------+-----------------------+
| ``token``             | Token                 | token reference       |
+-----------------------+-----------------------+-----------------------+
| ``volume``            | BigDecimal            | amount of token       |
|                       |                       | swapped across        |
|                       |                       | related pairs         |
+-----------------------+-----------------------+-----------------------+
| ``volumeETH``         | BigDecimal            | amount of token       |
|                       |                       | swapped across        |
|                       |                       | related pairs stored  |
|                       |                       | as a derived amount   |
|                       |                       | of ETH                |
+-----------------------+-----------------------+-----------------------+
| ``volumeUSD``         | BigDecimal            | amount of token       |
|                       |                       | swapped across        |
|                       |                       | related pairs stored  |
|                       |                       | as a derived amount   |
|                       |                       | of USD                |
+-----------------------+-----------------------+-----------------------+
| ``txCount``           | BigInt                | amount of             |
|                       |                       | transactions with     |
|                       |                       | this token across     |
|                       |                       | related pairs         |
+-----------------------+-----------------------+-----------------------+
| ``liquidity``         | BigDecimal            | amount of tokens      |
|                       |                       | deposited across      |
|                       |                       | related pairs         |
+-----------------------+-----------------------+-----------------------+
| ``liquidityETH``      | BigDecimal            | amount of tokens      |
|                       |                       | deposited across      |
|                       |                       | related pairs stored  |
|                       |                       | as ETH                |
+-----------------------+-----------------------+-----------------------+
| ``liquidityUSD``      | BigDecimal            | amount of tokens      |
|                       |                       | deposited across      |
|                       |                       | related pairs stored  |
|                       |                       | as USD                |
+-----------------------+-----------------------+-----------------------+
| ``priceUSD``          | BigInt                | token price in USD    |
+-----------------------+-----------------------+-----------------------+

TokenHourData
~~~~~~~~~~~~~

+--------+------+------------------------------------------------------+
| Field  | Type | Description                                          |
+========+======+======================================================+
| ``id`` | ID   | hour start timestamp concatenated with date          |
+--------+------+------------------------------------------------------+
| ``     | Int  | unix timestamp for the start of the hour             |
| date`` |      |                                                      |
+--------+------+------------------------------------------------------+
| ``t    | T    | token reference                                      |
| oken`` | oken |                                                      |
+--------+------+------------------------------------------------------+
| ``vo   | Bi   | amount of token swapped across related pairs         |
| lume`` | gDec |                                                      |
|        | imal |                                                      |
+--------+------+------------------------------------------------------+
| `      | Bi   | amount of token swapped across related pairs stored  |
| `volum | gDec | as a derived amount of ETH                           |
| eETH`` | imal |                                                      |
+--------+------+------------------------------------------------------+
| `      | Bi   | amount of token swapped across related pairs stored  |
| `volum | gDec | as a derived amount of USD                           |
| eUSD`` | imal |                                                      |
+--------+------+------------------------------------------------------+
| ``txC  | Bi   | amount of transactions with this token across        |
| ount`` | gInt | related pairs                                        |
+--------+------+------------------------------------------------------+
| `      | Bi   | amount of tokens deposited across related pairs      |
| `liqui | gDec |                                                      |
| dity`` | imal |                                                      |
+--------+------+------------------------------------------------------+
| ``li   | Bi   | amount of tokens deposited across related pairs      |
| quidit | gDec | stored as ETH                                        |
| yETH`` | imal |                                                      |
+--------+------+------------------------------------------------------+
| ``li   | Bi   | amount of tokens deposited across related pairs      |
| quidit | gDec | stored as USD                                        |
| yUSD`` | imal |                                                      |
+--------+------+------------------------------------------------------+
| ``pric | Bi   | token price in USD                                   |
| eUSD`` | gInt |                                                      |
+--------+------+------------------------------------------------------+
