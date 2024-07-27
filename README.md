# EpicChain Node README

Welcome to the EpicChain Node! This document provides comprehensive instructions for setting up, compiling, and using the EpicChain Node software. Follow these guidelines to ensure a smooth installation and operation of your node.

## Prerequisites

Before you start, ensure you have the correct environment for running the EpicChain Node:

- **Operating Systems:** 
  - **Windows**
  - **Linux** (Ubuntu 14 and 16 are supported; Ubuntu 17 is not supported)
  - **Mac** (If you are using a Mac, please use a virtual machine to run a supported version of Linux)

### Install .NET Core

EpicChain Node requires .NET Core to run. Please download and install the latest version of [.NET Core](https://www.microsoft.com/net/download/core) suitable for your operating system. This runtime environment is essential for executing the EpicChain Node application.

### Install Required Packages

#### On Linux

For Linux users, particularly those running Ubuntu 14 or 16, you need to install several development packages required for EpicChain Node:

1. Open a terminal window.
2. Execute the following command to install LevelDB and SQLite3 development libraries:

   ```sh
   sudo apt-get install libleveldb-dev sqlite3 libsqlite3-dev libunwind8-dev
   ```

   This command will download and install the necessary libraries that EpicChain Node depends on for data storage and management.

#### On Windows

If you are using Windows, you will need a specific version of LevelDB designed for EpicChain. Please download it from the following link:

- [EpicChain Version of LevelDB](https://github.com/xmoohad/leveldb)

Follow the instructions on the LevelDB GitHub page to properly install and integrate it into your system.

### Running EpicChain CLI

After installing the necessary components, you can start the EpicChain CLI (Command Line Interface) application. Open a command prompt or terminal and execute the following command:

```sh
dotnet epicchain-cli.dll
```

This command starts the EpicChain Node application, allowing you to interact with the blockchain and perform various operations.

## Compile from Source

If you prefer to compile EpicChain Node from source, follow these detailed steps:

1. **Clone the Repository**

   First, you need to clone the `epicchain-cli` repository from GitHub. Open your terminal or command prompt and run:

   ```sh
   git clone https://github.com/xmoohad/epicchain-cli.git
   ```

   Navigate into the cloned directory:

   ```sh
   cd epicchain-cli
   ```

2. **Restore Dependencies and Build**

   With the repository cloned, restore the required dependencies and compile the application. Execute the following commands:

   ```sh
   dotnet restore
   dotnet publish -c Release
   ```

   These commands will restore the necessary packages and build the project in release mode, preparing it for production use.

3. **.NET Core SDK**

   Ensure that you have version 1.1.2 of the .NET Core SDK installed on your system. If you need to download it, use the [SDK binary](https://www.microsoft.com/net/download/linux) provided on the .NET Core website.

   After downloading and extracting the .NET SDK, you can run the compiled application with:

   ```sh
   ../dotnet bin/Release/net8.0/epicchain-cli.dll .
   ```

   Adjust the path if necessary to match where you extracted the .NET SDK.

## Usage

Once your EpicChain Node is set up and running, you can use it to perform various operations. Below are some basic commands to get you started:

- **Show Node State**

  To check the current state of your EpicChain Node, use the following command:

  ```sh
  epicchain-cli.dll show state
  ```

  This command provides detailed information about the node’s current status, including blockchain synchronization, active connections, and more.

- **Create a New Wallet**

  To create a new wallet for managing your EpicChain assets, execute:

  ```sh
  epicchain-cli.dll create wallet wallet.db3
  ```

  Replace `wallet.db3` with the desired name for your wallet file. This command generates a new wallet database file, which will be used to store your blockchain assets securely.

## Conclusion

Thank you for choosing EpicChain Node! This README has provided you with the essential information needed to set up, compile, and use the node software. If you encounter any issues during installation or operation, please refer to the official documentation, visit the EpicChain community forums, or reach out for support. Your contribution to the EpicChain network is valuable, and we appreciate your involvement in building a decentralized future.