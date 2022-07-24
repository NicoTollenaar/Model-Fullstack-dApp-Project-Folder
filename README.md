# Model project folder for full-stack dApp

This is a model project folder for creating a full-stack dapp using:

- Frontend: Reactjs
- Backend: Nodejs / expressjs
- Database: MongoDb / Mongoose
- Blockchain/smart contract: EVM/solidity
- Interaction blockchain/smart contract: ethersjs

The folder was created using the ironlauncher package, see: https://www.npmjs.com/package/ironlauncher

The option was used that creates a react app (Creat React App), running the command: `npx ironlauncher@latest new-app --fs`

The option was selected that includes basic authentication routes.

Inside the "client" sub-directory a hardhat development environment was created following the instructions in this article by Naber Dabit: https://dev.to/dabit3/the-complete-guide-to-full-stack-ethereum-development-3j13

Instead of using the hardhat environment mentioned in this article, the new hardhat toolbox was used: https://hardhat.org/hardhat-runner/plugins/nomicfoundation-hardhat-toolbox

The hardhat toolbox was installed in the "client" subdirectory, but running the command: `npm install --save-dev @nomicfoundation/hardhat-toolbox`

The hardhat configurations have to be adjusted as explained in the abovementioned article of Naber Dabit to ensure that the artifacts end up in the "src" directory of the React App.

The hardhatconfig.js file was updated as follows:

`module.exports = { solidity: "0.8.4", paths: { artifacts: './src/artifacts', }, networks: { hardhat: { chainId: 1337 } } };`

The node_modules folders in the "client" and "server" sub-directories were removed. To re-install run `npm install` in both of these sub-directories that contain package.json files.
