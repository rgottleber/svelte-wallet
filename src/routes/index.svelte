<script>
	import WalletConnect from '$lib/WalletConnect.svelte';
	export let web3Props = { provider: null, signer: null, account: null, chainId: null };
</script>

<WalletConnect bind:web3Props />
