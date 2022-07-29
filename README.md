# @rgottleber/svelte-wallet
![npm](https://img.shields.io/npm/v/@rgottleber/wallet-connect)
[![GitHub issues](https://img.shields.io/github/issues/rgottleber/svelte-wallet)](https://github.com/rgottleber/svelte-wallet/issues)
[![GitHub license](https://img.shields.io/github/license/rgottleber/svelte-wallet)](https://github.com/rgottleber/svelte-wallet)

Single component to connect web3 wallet in Svelte

## Install
`npm install @rgottleber/svelte-wallet-connect`

## Usage
```html
<script>
    import { WalletConnect } from '@rgottleber/wallet-connect';
    export let web3Props = {
            provider: null,
            signer: null,
            account: null,
            chainId: null,
            contract: null
        };
</script>

<WalletConnect bind:web3Props />
```

## Other Info
The button includes `class="btn"` for styling purposes. As well as style variable. `<WalletConnect {style} bind:web3Props>`