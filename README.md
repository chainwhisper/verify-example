# Verify your contract on Binance Smart Chain


1. Install the [plugin](https://github.com/rkalis/truffle-plugin-verify) with `npm`

```
npm install -D truffle-plugin-verify
```

Make sure the version is >=`v 0.5.4`

2. Add the plugin to your truffle-config.js file
```
module.exports = {
  /* ... rest of truffle-config */

  plugins: [
    'truffle-plugin-verify'
  ]
}
```
3. Generate an API Key on your BSCscan account

If you don't have one yet, just go to [this page](https://bscscan.com/login) to sign up.


Add your BSCscan API key to your truffle config

```
module.exports = {
  /* ... rest of truffle-config */

  api_keys: {
    bscscan: 'MY_API_KEY'
  }
}
```

4.  Deploy your contract

```
truffle compile
truffle migrate --network testnet
```

5. Verify your contract

```
truffle run verify BEP20Token@{deployed-address} --network testnet

```