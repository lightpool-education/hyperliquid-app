# Tokenized Stocks App

**tokenized-stocks-app** implements a **Hyperliquid-style CLOB** for tokenized stocks on LightPool—on-chain trading that feels as smooth as a CEX, without wallet popups on every order, and built for high-frequency bot trading.

```bash
mkdir -p lightpool-labs && cd lightpool-labs
git clone git@github.com:lightpool-labs/tokenized-stocks-app.git
cd tokenized-stocks-app
```

## Step 1

Install the toolchain. Tools that are already installed are skipped.

```bash
./scripts/download-toolchain.sh
```

## Step 2

Download the other repositories and build them. Repositories that are already cloned are skipped.

```bash
./scripts/download-and-build.sh
```

The script clones these repositories next to this app: `lightpool-node`, `lightpool-crypto`, `lightpool-sdk-rust`, `lightpool-clob-indexer`, `lightpool-bridge`, `lightpool-bot`, and `lightpool-tutorials`. It then downloads Reth and builds the node, indexer, bridge, liquidity maker, and app backend.

## Step 3

Start the local stack.

```bash
./scripts/start-stocks.sh start
```

Open http://127.0.0.1:3000

Stop:

```bash
./scripts/start-stocks.sh stop
```

Delete runtime data (stop first):

```bash
./scripts/start-stocks.sh clean
```
