# DEX Candles Subgraph

This subgraph tracks all the DEX trades with 5m/15m/1h/4h/1d/1w candles.

## Protocols

- [x] Uniswap V2
- [ ] Uniswap V1
- [ ] Mooniswap
- [ ] 1inch Liquidity Protocol 1.0
- [ ] 1inch Liquidity Protocol 1.1
- [ ] Kyber Network
- [ ] Bancor Network
- [ ] 0x Protocol (excluding private orders)
- [ ] Oasis

## Schema

```graphql
type Candle @entity {
    id: ID! # time + period + srcToken + dstToken
    time: Int!
    period: Int!
    token0TotalAmount: BigInt!
    token1TotalAmount: BigInt!
    open: BigDecimal!
    close: BigDecimal!
    low: BigDecimal!
    high: BigDecimal!
}
```
