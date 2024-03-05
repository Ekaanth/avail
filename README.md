<div align="Center">
<h1>Avail Node</h1>
<h3>Official Client for the Avail blockchain</h3>
</div>

<br>

[![Build status](https://github.com/availproject/avail/actions/workflows/default.yml/badge.svg)](https://github.com/availproject/avail/actions/workflows/default.yml)


![demo](./.github/img/terminal.jpg)

## Running Avail Node
### Manually

> To manually run the Avail Node, you'll need to have the following dependencies installed:
> - [Rust](https://www.rust-lang.org/learn/get-started)
> - [Substrate dependencies](https://docs.substrate.io/install/)

Build the node binary
```
cargo build --release
```

After ensuring you have the dependencies installed, you can run the Avail Node using the following command:
```bash
mkdir -p output
cargo run --bin avail-node --locked --release -- --chain goldberg -d ./output
```
This command compiles and runs the Avail Node connected to the Goldberg Network.

```
2024-03-06 01:21:16 Avail Node    
2024-03-06 01:21:16 ✌️  version 2.0.0-b9e12941fbb    
2024-03-06 01:21:16 ❤️  by Avail Team, 2017-2024    
2024-03-06 01:21:16 📋 Chain specification: Avail Development Network    
2024-03-06 01:21:16 🏷  Node name: spiritual-box-4451    
2024-03-06 01:21:16 👤 Role: AUTHORITY    
2024-03-06 01:21:16 💾 Database: ParityDb at /tmp/substrateRdcjpi/chains/avail_development_network/paritydb/full    
2024-03-06 01:21:18 [0] 💸 generated 1 npos voters, 1 from validators and 0 nominators    
2024-03-06 01:21:18 [0] 💸 generated 1 npos targets    
2024-03-06 01:21:18 🔨 Initializing Genesis block/state (state: 0x535f…f4be, header-hash: 0x4040…60c7)    
2024-03-06 01:21:18 👴 Loading GRANDPA authority set from genesis on what appears to be first startup.    
2024-03-06 01:21:19 👶 Creating empty BABE epoch changes on what appears to be first startup.    
2024-03-06 01:21:19 🏷  Local node identity is: 12D3KooWAHwRDdRS5t9TfkF1j1W9MEqDLvyLFDvris5Uz3ioUnXe    
2024-03-06 01:21:19 Prometheus metrics extended with avail metrics    
2024-03-06 01:21:19 💻 Operating system: macos    
2024-03-06 01:21:19 💻 CPU architecture: aarch64    
2024-03-06 01:21:19 📦 Highest known block at #0    
2024-03-06 01:21:19 〽️ Prometheus exporter started at 127.0.0.1:9615    
2024-03-06 01:21:19 Running JSON-RPC server: addr=127.0.0.1:9944, allowed origins=["*"]    
2024-03-06 01:21:19 🏁 CPU score: 933.28 MiBs    
2024-03-06 01:21:19 🏁 Memory score: 39.50 GiBs    
2024-03-06 01:21:19 🏁 Disk score (seq. writes): 1.96 GiBs    
2024-03-06 01:21:19 🏁 Disk score (rand. writes): 437.16 MiBs    
2024-03-06 01:21:19 👶 Starting BABE Authorship worker    
2024-03-06 01:21:20 🙌 Starting consensus session on top of parent 0x40406cb985cc7aab47676de44c575eeca197104c066656e2c4fbdef4be1560c7    
2024-03-06 01:21:20 🎁 Prepared block for proposing at 1 (101 ms) [hash: 0x98f2b756cb3476419d32212d69b3c804362ee9284033dada10f86d0b540d2fca; parent_hash: 0x4040…60c7; extrinsics (1): [0x45f9…994f]    
2024-03-06 01:21:20 🔖 Pre-sealed block for proposal at 1. Hash now 0xcd233131c438543127213e70b7180a3aafc1548d7e12953a1c87605226aa0a1c, previously 0x98f2b756cb3476419d32212d69b3c804362ee9284033dada10f86d0b540d2fca.    
2024-03-06 01:21:20 👶 New epoch 0 launching at block 0xcd23…0a1c (block slot 85483414 >= start slot 85483414).    
2024-03-06 01:21:20 👶 Next epoch starts at slot 85484134    
2024-03-06 01:21:20 ✨ Imported #1 (0xcd23…0a1c)    
2024-03-06 01:21:24 💤 Idle (0 peers), best: #1 (0xcd23…0a1c), finalized #0 (0x4040…60c7), ⬇ 0 ⬆ 0    
2024-03-06 01:21:29 💤 Idle (0 peers), best: #1 (0xcd23…0a1c), finalized #0 (0x4040…60c7), ⬇ 0 ⬆ 0    
2024-03-06 01:21:34 💤 Idle (0 peers), best: #1 (0xcd23…0a1c), finalized #0 (0x4040…60c7), ⬇ 0 ⬆ 0    
2024-03-06 01:21:39 💤 Idle (0 peers), best: #1 (0xcd23…0a1c), finalized #0 (0x4040…60c7), ⬇ 0 ⬆ 0    
2024-03-06 01:21:40 🙌 Starting consensus session on top of parent 0xcd233131c438543127213e70b7180a3aafc1548d7e12953a1c87605226aa0a1c    
2024-03-06 01:21:40 🎁 Prepared block for proposing at 2 (4 ms) [hash: 0x3ede6259943162cd9534f95adbc895a76df2fba9a54380ba0a1ef2b39e10b0a8; parent_hash: 0xcd23…0a1c; extrinsics (1): [0x3487…3b88]    
2024-03-06 01:21:40 🔖 Pre-sealed block for proposal at 2. Hash now 0x80402ed8087db54725fff3d158cf25969ce4fedc73407c046b2b01b2db53ed31, previously 0x3ede6259943162cd9534f95adbc895a76df2fba9a54380ba0a1ef2b39e10b0a8. 
```

#### Running Dev Chain
A development chain is typically used for testing and development purposes.
```bash
cargo run --bin avail-node --locked --release -- --dev
```

### Docker
To run the Avail Node using Docker, follow these steps:

```bash
# Build the Docker image for the Avail Node:
docker build -t availnode -f ./dockerfiles/avail-node.Dockerfile .

# Create an output directory. Here the node's data will be stored.
mkdir output

# Run the Avail Node container:
docker run --rm -p 30333:30333 -p 9944:9944 -v ./output:/output availnode
# For SELinux
docker run --rm -p 30333:30333 -p 9944:9944 -v ./output:/output:z availnode
```

#### Running Dev Chain
There are instructions for running a development chain using Docker. A development chain is typically used for testing and development purposes.

```bash
# Build the Docker image for the Avail Node:
docker build -t availnode -f ./dockerfiles/avail-node.Dockerfile .

# Create an output directory. Here the node's data will be stored.
mkdir output

# Run the Avail Node container:
docker run --rm -p 30333:30333 -p 9944:9944 -v ./output:/output availnode --dev --rpc-methods=unsafe --unsafe-rpc-external --rpc-cors=all
# For SELinux
docker run --rm -p 30333:30333 -p 9944:9944 -v ./output:/output:z availnode --dev --rpc-methods=unsafe --unsafe-rpc-external --rpc-cors=all
```

### Podman
To run the Avail Node using Docker, follow these steps:

```bash
# Build the Docker image for the Avail Node:
podman build -t availnode -f ./dockerfiles/avail-node.Dockerfile .

# Create an output directory. Here the node's data will be stored.
mkdir output

# Run the Avail Node container:
podman run --rm -p 30333:30333 -p 9944:9944 -v ./output:/output availnode
# For SELinux
podman run --rm -p 30333:30333 -p 9944:9944 -v ./output:/output:z availnode
```

#### Running Dev Chain
There are instructions for running a development chain using Podman. A development chain is typically used for testing and development purposes.

```bash
# Build the Docker image for the Avail Node:
podman build -t availnode -f ./dockerfiles/avail-node.Dockerfile .

# Create an output directory. Here the node's data will be stored.
mkdir output

# Run the Avail Node container:
podman run --rm -p 30333:30333 -p 9944:9944 -v ./output:/output availnode --dev --rpc-methods=unsafe --unsafe-rpc-external --rpc-cors=all
# For SELinux
podman run --rm -p 30333:30333 -p 9944:9944 -v ./output:/output:z availnode --dev --rpc-methods=unsafe --unsafe-rpc-external --rpc-cors=all
```

## Kate RPC
To enable Kate RPC you need to pass `--enable-kate-rpc` flag when executing the binary.
```bash
./avail-node --enable-kate-rpc
```

## Run Benchmarks
### Kate RPC
```bash
./avail-node --dev --enable-kate-rpc-metrics
deno run -A ./examples/deno/benchmarks/query_proof.ts && deno run -A ./examples/deno/benchmarks/query_rows.ts && deno run -A ./examples/deno/benchmarks/query_block_length.ts && deno run -A ./examples/deno/benchmarks/query_app_data.ts && deno run -A ./examples/deno/benchmarks/query_data_proof_v2.ts
```

### Header Builder
```bash
# Option 1: for time measurement 
cargo bench --bench header_kate_commitment_cri
# Option 2: for time measurement 
cargo bench --bench header_kate_commitment_divan
# Option 1: for instructions, cache and main memory hits
cargo bench --bench header_kate_commitment_iai_callgrind
# Option 2: for instructions, cache and main memory hits
cargo bench --bench header_kate_commitment_iai
```

## Additional Documentation
For additional documentation check our [wiki page](https://github.com/availproject/avail/wiki).
There you can learn how to:
- Run Avail Node together with Avail Light Clients
- Build Avail Node for different Linux flavours
- Find out what node synchronization options are available
- Running Avail Benchmarks


## Interact with the chain
You can find on this repository many example on how to interract with any avail chain.
- In the avail-js folder, you will find our wrapper for polkadot js including multiple helpers.
    - The example folder contains some examples using node-js and an example web app to setup the extension.
- In the avail-subxt folder, you will find our fork of subxt with some example on usage.
- In the examples folders you will find examples for:
  - Deno examples
  - Go examples
  - Validium example implementation 