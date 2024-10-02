# RWA (Real World Asset) DApp

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Architecture](#architecture)
- [Testing](#testing)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

This decentralized application (DApp) combines the Loandisk API with a Bitcloud-react frontend to tokenize and manage Real World Assets (RWAs) on the blockchain. It utilizes Chainlink Functions and CCIP (Cross-Chain Interoperability Protocol) to connect RWAs provided by Loandisk, with Thirdweb serving as middleware and smart contract facilitator.

## Features

- User authentication via Web3 wallets
- Real World Asset listing and details view
- Asset tokenization (minting) on the blockchain
- Cross-chain asset transfers using Chainlink CCIP
- Integration with Loandisk API for real-world asset data
- User dashboard for managing tokenized assets
- Responsive design for mobile and desktop

## Prerequisites

- Node.js (v14.0.0 or later)
- npm (v6.0.0 or later)
- MetaMask or another Web3 wallet
- Access to Loandisk API (API key required)

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/your-username/rwa-dapp.git
   cd rwa-dapp
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Create a `.env` file in the root directory and add the following variables:
   ```
   REACT_APP_LOANDISK_API_KEY=your_loandisk_api_key
   REACT_APP_RWA_CONTRACT_ADDRESS=your_contract_address
   REACT_APP_CHAINLINK_FUNCTION_ADDRESS=your_chainlink_function_address
   ```

## Configuration

1. Update the `src/config.js` file with your specific network and contract details.

2. If you're using a custom Chainlink Function, update the `src/utils/chainlinkFunctions.js` file with your function's logic.

## Usage

1. Start the development server:
   ```
   npm start
   ```

2. Open your browser and navigate to `http://localhost:3000`

3. Connect your Web3 wallet when prompted.

4. Explore available RWAs, mint tokens, and manage your assets through the dashboard.

## Architecture

This DApp follows a three-tier architecture:

1. Frontend: React-based UI using Bitcloud components
2. Middleware: Thirdweb SDK for blockchain interactions
3. Backend: Smart contracts on Ethereum (or other supported chains), IPFS for decentralized storage, and Chainlink for off-chain computations and cross-chain communication

For a detailed system diagram, refer to the `docs/system-architecture.md` file.

## Testing

Run the test suite:

```
npm test
```

For end-to-end testing, we use Cypress. Run e2e tests with:

```
npm run test:e2e
```

## Deployment

1. Build the project:
   ```
   npm run build
   ```

2. Deploy the built files in the `build` directory to your preferred hosting service (e.g., Netlify, Vercel, or AWS S3).

3. Ensure your smart contracts are deployed to the desired network(s) and update the `.env` file accordingly.

## Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for more details.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any queries or support, please open an issue on this repository or contact the maintainers at: support@rwa-dapp.com
