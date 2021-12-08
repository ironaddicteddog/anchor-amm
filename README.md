# Anchor Example: Token Swap AMM

SPL [Token-swap](https://github.com/solana-labs/solana-program-library/tree/master/token-swap) (AMM) implemented in Anchor.

## Build, Deploy and Test

First, install dependencies:

```
$ yarn
```

Next, we will build and deploy the program via Anchor.

Get the program ID:

```
$ anchor keys list
anchor_amm: 4CkSf34hTH2rGmgFDCm5WCFE8sHpfdBzrBChEScJBxoM
```

Here, make sure you update your program ID in `Anchor.toml` and `lib.rs`.

Build the program:

```
$ anchor build
```

Let's deploy the program. Notice that `anchor-amm` will be deployed on a [mainnet-fork](https://github.com/DappioWonderland/solana) test validator run by Dappio:

```
$ anchor deploy
...

Program Id: 4CkSf34hTH2rGmgFDCm5WCFE8sHpfdBzrBChEScJBxoM

Deploy success
```

Finally, run the test:

```
$ anchor test --skip-build --skip-deploy
```
