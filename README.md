# how-to-run-da-retriever

![1_7gPDdUg77wgro3bYJwtNwQ](https://github.com/user-attachments/assets/ff425b2f-75e2-4327-a221-4a29a7f78c67)


## Hardware Requirement
```bash
- RAM: 8 GB
- CPU: 2 cores
- Bandwidth: 100 MBps for Download / Upload
```

## Install Dependencies
```bash
sudo apt-get update
sudo apt-get install cmake build-essential protobuf-compiler
```

Install Rust
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

## Donwload the Source Code
```bash
git clone https://github.com/0glabs/0g-da-retriever.git
```

## Configuration
|Field|Description|
|:----|:----------|
|`log_level`|Set log level|
|`grpc_listen_address`|Server listening address.|
|`eth_rpc_endpoint`|JSON RPC node endpoint for the blockchain network.|

## Build
```bash
cargo build --release
```

## Run
```bash
./target/release/retriever --config ./run/config.toml
```

# END
You're doing great to make it all the way up here! Subscribe to my social media and stay tuned for updates!

- Twitter - https://x.com/cutegina0118
- Medium - https://medium.com/@sergenode
- My Discord Profile - https://discord.com/users/960029203468795914
