# Stellar_Finance_App

# Welcome to the Lumen Finance Stellar App Documentation

This documentation provides a guide to getting started with the Lumen Finance Stellar App, a decentralized application built with Next.js and leveraging the power of the Stellar network and Soroban smart contracts.

## Getting Started

To initiate the development environment, execute the following command within your project directory using your preferred package manager:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev

Upon successful execution, the application will be accessible in your web browser at http://localhost:3000.
Developing the Application

Begin customizing the user interface and application logic by modifying files within the pages/ and components/ directories. Changes made to these files will be automatically reflected in the running application, facilitating a rapid development cycle.

While this application primarily interacts with on-chain smart contracts, you can implement frontend API routes within the pages/api/ directory. These routes are accessible at http://localhost:3000/api/* and can be utilized for integrating with external services or managing application-specific backend logic that is separate from the decentralized contract interactions. Example API endpoints can be defined and modified within pages/api/.

This project is configured to utilize next/font for optimized font delivery, currently employing Inter, a versatile Google Font, to enhance the application's typography and user experience.
Interacting with the Lumen Finance Smart Contract

This application is designed to interact with a deployed Soroban smart contract on the Stellar network. Below are example commands for deploying and interacting with the Lumen Finance contract on the Testnet environment.

Example Contract Deployment (Testnet):

Before deploying, ensure you have the Stellar CLI (stellar) installed and configured to interact with the Testnet network.

1. Install the Smart Contract WASM:

This command installs the compiled WebAssembly (WASM) code of the Lumen Finance contract onto the Stellar network. Replace bob with the Stellar account you are using as the deployer.


stellar contract install \
  --network testnet \
  --source bob \
  --wasm target/wasm32-unknown-unknown/release/lumen_finance_contract.wasm
  
 2. Deploy the Smart Contract Instance:

This command deploys an instance of the Lumen Finance contract using the WASM hash obtained from the installation step. Replace 29aa140eb8fd57df7bd0ca2366e115752970310b26d290135a3796e66663a693 with the actual WASM hash returned by the contract install command, and bob with your deployer account.


Upon successful deployment, the command will output the Lumen Finance Contract ID. This ID is crucial for interacting with your deployed contract instance from the application.

Example Lumen Finance Contract ID (Testnet - Example Only):

      
CDLCXVC4JPATLFEOQGY736RQLT3MWMM2QC46CRI36FL4HZA35UU3E5UO

    

IGNORE_WHEN_COPYING_START
Use code with caution.
IGNORE_WHEN_COPYING_END

Soroban Token Hash (Example - USDC Test Token):

This is an example hash for a Soroban-based USDC token contract, often used for testing and development on the Stellar network.

      
c6fe61fb6c64cbe3e23cb52b059d43545875cf1bc2d396c6d901cfa51a712033

    

IGNORE_WHEN_COPYING_START
Use code with caution.
IGNORE_WHEN_COPYING_END

Soroban USDC Token Address (Example - Testnet):

This is an example address for a deployed Soroban USDC token contract on the Testnet. You may need to deploy or utilize a different token contract depending on your application's requirements.

      
CD7DUUEY7CJ3K62T5N3WD7KMGKJMMRRKLH3B27Z2MHQT2VR2IPQABZHM

    

IGNORE_WHEN_COPYING_START
Use code with caution.
IGNORE_WHEN_COPYING_END

Note: The Contract ID, Token Hash, and Token Address provided above are examples for illustrative purposes and may not be actively deployed or functional. You will need to deploy your own Lumen Finance contract and potentially other Soroban-based tokens for a fully functional application.
Further Exploration

To deepen your understanding of the technologies powering this application, we recommend exploring the following resources:

    Next.js Documentation: Comprehensive documentation covering all aspects of the Next.js framework, its features, and API: https://nextjs.org/docs

    Learn Next.js: An interactive tutorial designed to guide you through the fundamentals of Next.js development: https://nextjs.org/learn

    Stellar Documentation: Official documentation for the Stellar network, covering concepts, protocols, and development tools: https://developers.stellar.org/docs

    Soroban Documentation: Documentation specific to Soroban, Stellar's smart contract platform, including contract development, deployment, and interaction: https://soroban.stellar.org/docs

    Stellar GitHub Repository: Explore the open-source codebase of Stellar and contribute to the ecosystem: https://github.com/stellar

Deployment Considerations

For deploying your Lumen Finance Stellar App to a production environment, consider platforms optimized for Next.js applications and capable of interacting with the Stellar network. Refer to the Next.js deployment documentation and Stellar network guidelines for best practices and platform recommendations.

This documentation serves as a starting point for your journey with the Lumen Finance Stellar App. As you delve deeper into development, remember to consult the linked resources and community forums for further assistance and advanced techniques.

