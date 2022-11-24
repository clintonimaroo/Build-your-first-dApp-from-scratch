# Build-your-first-dApp-from-scratch
Build your first Hands-On Blockchain Application

## Getting Started

So before we get started, We need to create a new moralis server, Unfortunately it is not possible to create Moralis servers anymore on [moralis](https://moralis.io/). So for this project we are going to self-host our own servers. [How to self host your Moralis server](https://docs.moralis.io/docs/run-parse-server-locally).

Once you have successful hosted your moralis server, now let's jump to the next stage.

## Build Your First dApp – Code

- Since we have hosted our [moralis server](https://moralis.io/). So now we need to include the Moralis code into our dApp, To do this we will start with a basic HTML structure.

```html

// Get the balance of an ERC20 token.
const data = await multichainWallet.getBalance({
  address: '0x2455eC6700092991Ce0782365A89d5Cd89c8Fa22',
  network: 'ethereum',
  rpcUrl: 'https://rpc.ankr.com/eth',
  tokenAddress: '0xdac17f958d2ee523a2206206994597c13d831ec7',
}); // NOTE - For other EVM compatible blockchains all you have to do is change the rpcUrl.


// Get the balance of a token on Solana.
const data = await multichainWallet.getBalance({
  address: '5PwN5k7hin2XxUUaXveur7jSe5qt2mkWinp1JEiv8xYu',
  tokenAddress: 'Es9vMFrzaCERmJfrF4H2FYD4KCoNkY11McCe8BenwNYB',
  network: 'solana',
  rpcUrl: 'https://rpc.ankr.com/solana',
});

// Get the balance of a token on Waves.
const data = await multichainWallet.getBalance({
  network: 'waves',
  address: '3NBE5tjbQn9BHczjD6NSSuFDKVHKsBRzTv9',
  rpcUrl: 'https://nodes-testnet.wavesnodes.com',
  tokenAddress: '39pnv8FVf3BX3xwtC6uhFxffy2sE3seXCPsf25eNn6qG',
});
```

- Install dependencies with  
