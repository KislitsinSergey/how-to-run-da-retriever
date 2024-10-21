# How to run node for Rebus chain

## Setting Up a Validator Node for Rebus

### Prerequisites

1. **System Requirements**
   - Ubuntu 20.04 or later
   - At least 4 GB RAM
   - 2 CPU cores
   - 50 GB SSD
   - Go installed (version 1.18+)

2. **Install Go**
   ```bash
   sudo apt update
   sudo apt install golang-go
   ```

3. **Install Git**
   ```bash
   sudo apt install git
   ```

### Clone the Rebus Repository

1. Navigate to your working directory:
   ```bash
   cd ~
   ```

2. Clone the Rebus repository:
   ```bash
   git clone https://github.com/rebuschain/rebus
   cd rebus
   ```

### Build the Validator Binary

1. Build the project:
   ```bash
   make install
   ```

   This will generate a binary named `rebusd` in your `$GOPATH/bin`.

### Initialize the Node

1. Initialize the node:
   ```bash
   rebusd init <your_moniker>
   ```

   Replace `<your_moniker>` with a name for your validator node.

### Configure the Node

1. Edit the configuration file located at `~/.rebus/config/config.toml`:
   ```bash
   nano ~/.rebus/config/config.toml
   ```

2. Set up the persistent peers:
   ```toml
   persistent_peers = "<peer_id>@<peer_address>"
   ```

   You can find peer IDs and addresses in the Rebus documentation or community channels.

### Download Genesis File

1. Download the latest genesis file:
   ```bash
   curl -o ~/.rebus/config/genesis.json https://path_to_genesis_file
   ```

2. Update the `seeds` configuration in `~/.rebus/config/config.toml`:
   ```toml
   seeds = "<seed_node_id>@<seed_node_address>"
   ```

### Create Validator Keys

1. Generate a new keypair:
   ```bash
   rebusd keys add <your_validator_key>
   ```

   Store your mnemonic securely!

### Start the Node

1. Start the Rebus validator node:
   ```bash
   rebusd start
   ```

### Monitoring and Logs

- You can monitor logs by checking the console output or viewing the log file at `~/.rebus/logs`.

### Additional Commands

- To check the status of your node:
  ```bash
  rebusd status
  ```

- To view your validator information:
  ```bash
  rebusd q staking validator <validator_address>
  ```

### Conclusion

You now have a basic validator node running for the Rebus project. Make sure to stay updated with the Rebus community for any changes or updates.

For more detailed information, refer to the [official documentation](https://docs.rebuschain.com/) and the [GitHub repository](https://github.com/rebuschain).

Feel free to reach out if you have any questions!
```

# END
You're doing great to make it all the way up here! Subscribe to my social media and stay tuned for updates!

- Twitter - https://x.com/cutegina0118
- Medium - https://medium.com/@sergenode
- My Discord Profile - https://discord.com/users/960029203468795914
