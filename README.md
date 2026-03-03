# bZx Protocol Flash Loan Exploit — PoC

> **Educational Purpose Only** — This PoC is created for security research and education
> purposes only. It runs against a fork, not mainnet.

## Quick Start

```bash
git clone https://github.com/NomosLabs-Security/poc-bzx-protocol-2020
cd poc-bzx-protocol-2020
forge install foundry-rs/forge-std --no-git
forge test -vvvv
```

## Details

- **Exploit Date:** 2020-02-15
- **Fork Block:** #9484688
- **Expected Output:** Flash loan → margin trade → oracle manipulation → profit
- **Full Analysis:** [NomosLabs Security Intelligence Archive](https://nomoslabs.io/archive/bzx-protocol-2020)

## Description

bZx was one of the first DeFi protocols exploited via flash loans. The attacker:

1. Flash borrowed 10,000 ETH from dYdX
2. Used 5,500 ETH as collateral on Compound to borrow 112 WBTC
3. Opened a 5x short ETH/BTC position on bZx (using remaining 1,300 ETH)
4. The large sell on Uniswap pushed ETH/BTC price down
5. Profited from the WBTC loan + short position

## License

MIT — For educational use only.
