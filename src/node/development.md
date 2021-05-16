# Development

## Build

Install Rust:

```bash
curl https://sh.rustup.rs -sSf | sh
```

NOTE: change install setting [default toolchain: stable (default)] -> nightly.

```bash
rustup default nightly
```

Clone Code:

```bash
git clone https://github.com/parami-protocol/parami.git
cd parami
git submodule init
git submodule update
```

Install required rust target(wasm32):

```bash
.maintain/init.sh
```

Build Parami:

```bash
cargo build --release
```

## Running a node

Ensure you have a fresh start if updating from another version:

```bash
./target/release/parami purge-chain
```

To start a Parami node, run:

```bash
./target/release/parami --chain resources/dana.v2.json
```

To start the Parami validater node, run:

```bash
./target/release/parami \
  --chain resources/dana.v2.json \
  --name NodeName \
  --validator \
  --node-key ..... \
  --keystore-path /path/to/auth
```

## Dev node

To start a local dev node, run:

```bash
cargo run --release -- --dev --alice --tmp
```

To start 2 local nodes, run:

```bash
cargo run -- --chain local --alice --tmp
```

And:

```bash
cargo run -- --chain local --bob --tmp --port 30334
```

In different terminal tab.
