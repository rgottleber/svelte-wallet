<script>
	import WalletConnect from 'wallet-connect';
	export let web3Props = { provider: null, signer: null, account: null, chainId: null };
</script>

<WalletConnect bind:web3Props />
