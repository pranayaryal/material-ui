# Material-UI benchmark

## `@material-ui/core`

### Synthetic benchmark

```sh
yarn core

ButtonBase cache instances x 37,666 ops/sec ±10.24% (64 runs sampled)
ButtonBase cache requests x 36,496 ops/sec ±6.27% (68 runs sampled)
ButtonBase no cache x 6,099 ops/sec ±4.62% (76 runs sampled)
JssButton cache requests x 79,646 ops/sec ±6.08% (70 runs sampled)
JssButton cache instances x 85,326 ops/sec ±8.94% (63 runs sampled)
JssButton no cache x 9,896 ops/sec ±6.01% (79 runs sampled)
JssButton no styles x 82,949 ops/sec ±4.40% (68 runs sampled)
HocButton x 126,784 ops/sec ±5.50% (66 runs sampled)
NakedButton x 182,888 ops/sec ±3.25% (51 runs sampled)
StyledButton x 17,752 ops/sec ±6.89% (81 runs sampled)
EmotionButton x 68,917 ops/sec ±19.32% (73 runs sampled)
ButtonBase cache x 34,618 ops/sec ±12.83% (68 runs sampled)
ButtonBase ripple x 38,715 ops/sec ±13.70% (68 runs sampled)
ButtonBase disableRipple x 46,165 ops/sec ±13.53% (66 runs sampled)
```

### Real-world benchmark

```sh
yarn server

bombardier \
  -c 4 \
  -l \
  -d 30s \
  -m GET \
  '0.0.0.0:3001/ui-box'

Statistics        Avg      Stdev        Max
  Reqs/sec       442.47      55.44     547.63
  Latency      225.64ms    17.11ms   471.31ms
  Latency Distribution
     50%   221.98ms
     75%   230.69ms
     90%   241.19ms
     95%   247.87ms
     99%   273.88ms
  HTTP codes:
    1xx - 0, 2xx - 26642, 3xx - 0, 4xx - 0, 5xx - 0
    others - 0
  Throughput:    11.61MB/s
```

## `@material-ui/system`

```sh
yarn system

@material-ui/system palette x 410,735 ops/sec ±2.05% (171 runs sampled)
styled-system color x 176,670 ops/sec ±1.96% (184 runs sampled)

@material-ui/system spacing x 320,001 ops/sec ±4.30% (186 runs sampled)
styled-system space x 130,870 ops/sec ±1.30% (186 runs sampled)

@material-ui/system composed x 70,434 ops/sec ±0.61% (191 runs sampled)
styled-system composed x 32,479 ops/sec ±0.83% (189 runs sampled)

@material-ui/system Box x 11,535 ops/sec ±1.52% (187 runs sampled)
@material-ui/styles Box x 12,469 ops/sec ±1.91% (188 runs sampled)
styled-system Box x 9,242 ops/sec ±0.80% (190 runs sampled)
```

## Resources

- [Bombardier](https://github.com/codesenberg/bombardier)
