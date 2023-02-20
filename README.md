# NebulaSwap Subgraph

TheGraph exposes a GraphQL endpoint to query the events and entities within the Binance Smart Chain and NebulaSwap ecosystem.

Currently, there are multiple subgraphs, but additional subgraphs can be added to this repository, following the current architecture.

## Subgraphs

1. **[Blocks](https://thegraph.com/legacy-explorer/subgraph/nebulaswap/blocks)**: Tracks all blocks on Binance Smart Chain.

2. **[Exchange](https://nodereal.io/meganode/api-marketplace/nebulaswap-graphql)**: Tracks all NebulaSwap Exchange data with price, volume, liquidity, ...

3. **[Farm Auctions](https://thegraph.com/legacy-explorer/subgraph/nebulaswap/farm-auctions)**: Tracks all NebulaSwap Farm Auctions with auctions and bids.

4. **[Lottery](https://thegraph.com/legacy-explorer/subgraph/nebulaswap/lottery)**: Tracks all NebulaSwap Lottery with rounds, draws and tickets.

5. **[NFT Market (v1)](https://thegraph.com/legacy-explorer/subgraph/nebulaswap/nft-market)**: Tracks all NebulaSwap NFT Market for ERC-721.

6. **[Pairs](https://thegraph.com/legacy-explorer/subgraph/nebulaswap/pairs)**: Tracks all NebulaSwap Pairs and Tokens.

7. **[Prediction (v1)](https://thegraph.com/legacy-explorer/subgraph/nebulaswap/prediction)**: Tracks all NebulaSwap Prediction (v1) with market, rounds, and bets.

8. **[Prediction (v2)](https://thegraph.com/legacy-explorer/subgraph/nebulaswap/prediction-v2)**: Tracks all NebulaSwap Prediction (v2) with market, rounds, and bets.

9. **[Profile](https://thegraph.com/legacy-explorer/subgraph/nebulaswap/profile)**: Tracks all NebulaSwap Profile with teams, users, points and campaigns.

10. **[SmartChef](https://thegraph.com/legacy-explorer/subgraph/nebulaswap/smartchef)**: Tracks all NebulaSwap SmartChef (a.k.a. Syrup Pools) with tokens and rewards.

11. **[Timelock](https://thegraph.com/legacy-explorer/subgraph/nebulaswap/timelock)**: Tracks all NebulaSwap Timelock queued, executed, and cancelled transactions.

12. **[Trading Competition (v1)](https://thegraph.com/legacy-explorer/subgraph/nebulaswap/trading-competition-v1)**: Tracks all metrics for the Easter Battle (April 07—14, 2021).

13. **[MasterChef (v2)](https://thegraph.com/hosted-service/subgraph/nebulaswap/masterchef-v2)**: Tracks data for MasterChefV2.


## Dependencies

- [Graph CLI](https://github.com/graphprotocol/graph-cli)
    - Required to generate and build local GraphQL dependencies.

```shell
yarn global add @graphprotocol/graph-cli
```

## Deployment

For any of the subgraph: `blocks` as `[subgraph]`

1. Run the `cd subgraphs/[subgraph]` command to move to the subgraph directory.

2. Run the `yarn codegen` command to prepare the TypeScript sources for the GraphQL (generated/*).

3. Run the `yarn build` command to build the subgraph, and check compilation errors before deploying.

4. Run `graph auth --product hosted-service '<ACCESS_TOKEN>'`

5. Deploy via `yarn deploy`.
