<script lang="ts">
	import { ethers } from 'ethers';
	export let style = '';
	export let web3Props = { provider: null, signer: null, account: null, chainId: null };
	async function connectWallet() {
		let provider = new ethers.providers.Web3Provider(window.ethereum, 'any');
		await provider.send('eth_requestAccounts', []);
		const signer = provider.getSigner();
		const account = await signer.getAddress();
		const chainId = await signer.getChainId();
		web3Props = { signer, provider, chainId, account };
	}
</script>

{#if !web3Props.account}
	<button {style} class="btn" on:click={connectWallet}>Attach Wallet</button>
{/if}
