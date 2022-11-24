# Build-your-first-dApp-from-scratch
Build your first Hands-On Blockchain Application

## Getting Started

So before we get started, We need to create a new moralis server, Unfortunately it is not possible to create Moralis servers anymore on [moralis](https://moralis.io/). So for this project we are going to self-host our own servers. [How to self host your Moralis server](https://docs.moralis.io/docs/run-parse-server-locally).

Once you have successful hosted your moralis server, now let's jump to the next stage.

## Prerequisites to run the website locally:

- [npm and node](https://docs.npmjs.com/cli/v8/configuring-npm/install)
- [yarn](https://marketplace.visualstudio.com/items?itemName=gamunu.vscode-yarn)

## Database:

- [mongodb](https://www.mongodb.com/)


## Build Your First dApp – Code

- Since we have hosted our [moralis server](https://moralis.io/). So now we need to include the Moralis code into our dApp, To do this we will start with a basic HTML structure.

```html

<!DOCTYPE html>
<html>
  <head>
    <title>Build your first dapp with moralis</title>
    <script src="https://cdn.jsdelivr.net/npm/web3@latest/dist/web3.min.js"></script>
    <script src="https://unpkg.com/moralis/dist/moralis.js"></script>
  </head>

  <body>
    <h1>Login</h1>

    <button onclick=”login()” id="login">Login</button>

    <script>
       const serverUrl = "https://localhost:xxxx/server";
       const appId = "YOUR_APP_ID"; //Your app id can be found in your [.env folder](https://moralis.io/)
       Moralis.start({ serverUrl, appId });

       async function login() {
           Await Moralis.authenticate()
       }

    </script>

  </body>
</html>

```

- Now, Let's run the code to access our dApp.
