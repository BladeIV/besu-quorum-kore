# besu-quorum-kore
Besu server with squickstart options from src build
# Quorum Genesis Tool - Updated Version

## Overview

The **Quorum Genesis Tool** is a utility to generate the necessary genesis files and configurations for setting up a private blockchain using Hyperledger Besu. This version has been updated to recommend **QBFT** as the preferred consensus mechanism and marks **Raft** as deprecated, providing guidance for users to make informed choices during setup.

This tool automates the creation of network configurations, including Docker Compose setups, to make development easier for blockchain developers and enthusiasts.

## Key Features
- Supports multiple consensus mechanisms, including **IBFT**, **IBFT2**, **QBFT (recommended)**, **Clique**, and **Raft (deprecated soon)**.
- Generates a complete genesis file based on the specified Chain ID.
- Automated Docker Compose configuration for seamless network deployment.
- Cross-chain bridge integration.

## Requirements
- **Node.js** (version 20 or above recommended)
- **npm**
- **Docker** and **Docker Compose**

### Dependencies Installation
- Ensure the following dependencies are installed before running the setup:
  - **Node.js**: Install the latest stable version from NodeSource.
  - **Docker**: Used for creating Besu nodes and cross-chain bridge service.
  - **Docker Compose**: Required to run multiple services in Docker.

## Installation
1. **Download the Repository**
   - Clone or download the repository to your local machine:
     ```sh
     git clone https://github.com/your-username/quorum-genesis-tool-updated.git
     cd quorum-genesis-tool-updated
     ```

2. **Install Dependencies**
   - Install the required Node.js dependencies:
     ```sh
     npm install
     ```

3. **Build the Project**
   - Build the TypeScript files to generate necessary JavaScript artifacts:
     ```sh
     npm run build
     ```

4. **Generate Genesis File**
   - Generate the genesis file with Chain ID 138:
     ```sh
     node ./dist/index.js --chain-id 138
     ```

## Usage
### Starting the Network
- Use **Docker Compose** to start the Besu nodes and cross-chain bridge services:
  ```sh
  docker-compose up -d
  ```

### Checking Network Status
- Verify the status of the Docker containers:
  ```sh
  docker ps
  ```
- To see logs for any running container:
  ```sh
  docker-compose logs -f
  ```

## Configuration Options
During setup, the tool will prompt users to choose from the following consensus algorithms:
- **IBFT**
- **IBFT2**
- **QBFT (recommended)**
- **Clique**
- **Raft (will be deprecated soon)**

> **Note**: QBFT is currently the recommended consensus algorithm, while Raft is marked as deprecated.

## Example Commands Recap
1. **Navigate to Project Directory**
   ```sh
   cd /path/to/quorum-genesis-tool-updated
   ```
2. **Install Dependencies**
   ```sh
   npm install
   ```
3. **Build the Project**
   ```sh
   npm run build
   ```
4. **Generate Genesis File**
   ```sh
   node ./dist/index.js --chain-id 138
   ```
5. **Start Docker Containers**
   ```sh
   docker-compose up -d
   ```

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contributing
We welcome contributions from the community! Feel free to fork the repository and submit a pull request for any features, improvements, or bug fixes.

## Contact
For questions or assistance, please open an issue in the repository or contact the project maintainer.

**Happy Building!** 🎉

