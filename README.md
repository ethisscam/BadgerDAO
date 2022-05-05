# BadgerDAO

## Balancer Gauge Pool
- get the pool info

endpoint:
https://api.thegraph.com/subgraphs/name/balancer-labs/balancer-v2/graphql
```
sql
{
  balancers(first: 500) {
    id
    pools(first: 500) {
      name
      totalLiquidity
      totalShares
      poolType
      tokens {
        symbol
        id
        balance
        weight
      }
      id
    }
    totalLiquidity
  }
}
```
endpoint:
https://api.thegraph.com/subgraphs/name/balancer-labs/balancer-gauges/graphql
sql:
```
{
  votingEscrows {
    stakedSupply
  }
  liquidityGauges {
    symbol
    poolAddress
    poolId
    totalSupply
    id
    shares {
      balance
    }
  }
}
```
  

