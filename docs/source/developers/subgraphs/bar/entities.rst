Entities
=========

Entities for the SHNDBar subgraph are all listed below.

Bar
---

====================== ========== ================================
Field                  Type       Description
====================== ========== ================================
``id``                 ID         id
``decimals``           BigInt     decimals
``name``               String     name
``sushi``              Bytes      address of sushi
``symbol``             String     symbol
``totalSupply``        BigDecimal total supply
``ratio``              BigDecimal ratio
``xSushiMinted``       BigDecimal amount of xSUSHI minted
``xSUSHIBurned``       BigDecimal amount of xSUSHI burned
``sushiStaked``        BigDecimal amount of SUSHI staked
``sushiStakedUSD``     BigDecimal amount of SUSHI staked in USD
``sushiHarvested``     BigDecimal amount of SUSHI harvested
``sushiHarvestedUSD``  BigDecimal amount of SUSHI harvested in USD
``xSushiAge``          BigDecimal age of the xSUSHI
``xSushiAgeDestroyed`` BigDecimal xSUSHI age destroyed
``users``              [Users]    array of users
``updatedAt``          BigInt     timestamp bar was updated at
====================== ========== ================================

User
----

+---------------------+----------+-------------------------------------+
| Field               | Type     | Description                         |
+=====================+==========+=====================================+
| ``id``              | ID       | id                                  |
+---------------------+----------+-------------------------------------+
| ``xSushi``          | Bi       | xSUSHI                              |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``xSushiIn``        | Bi       | amount of xSUSHI in                 |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``xSushiOut``       | Bi       | amount of xSUSHI out                |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``xSushiMinted``    | Bi       | amount of xSUSHI minted             |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``xSUSHIBurned``    | Bi       | amount of xSUSHI burned             |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``xSushiOffset``    | Bi       | xSUSHI offset                       |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``xSushiAge``       | Bi       | age of the xSUSHI                   |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``x                 | Bi       | xSUSHI age destroyed                |
| SushiAgeDestroyed`` | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``sushiStaked``     | Bi       | amount of SUSHI staked              |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``sushiStakedUSD``  | Bi       | amount of SUSHI staked in USD       |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``sushiHarvested``  | Bi       | amount of SUSHI harvested           |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``                  | Bi       | amount of SUSHI harvested in USD    |
| sushiHarvestedUSD`` | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``sushiOut``        | Bi       | amount of SUSHI out                 |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``sushiIn``         | Bi       | amount of SUSHI in                  |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``usdOut``          | Bi       | amount of USD out                   |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``usdIn``           | Bi       | amount of USD in                    |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``sushiOffset``     | Bi       | SUSHI offset                        |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``usdOffset``       | Bi       | USD offset                          |
|                     | gDecimal |                                     |
+---------------------+----------+-------------------------------------+
| ``createdAt``       | BigInt   | timestamp of when user was created  |
+---------------------+----------+-------------------------------------+
| ``createdAtBlock``  | BigInt   | block of when user was created      |
+---------------------+----------+-------------------------------------+
| ``updatedAt``       | BigInt   | timestamp of when user was updated  |
+---------------------+----------+-------------------------------------+
| ``updatedAtBlock``  | BigInt   | block of when user was updated      |
+---------------------+----------+-------------------------------------+
