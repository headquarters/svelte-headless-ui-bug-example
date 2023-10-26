<script>
	import {
		Dialog,
		DialogOverlay,
		DialogTitle,
		DialogDescription
	} from '@rgossiaux/svelte-headlessui';
	let isOpen = false;
</script>

<button type="button" on:click={() => (isOpen = true)}>Open Dialog</button>

<Dialog open={isOpen} on:close={() => (isOpen = false)} class="dialog">
	<DialogOverlay class="dialog-overlay" />

	<div class="dialog-content">
		<DialogTitle>Dialog Title</DialogTitle>
		<p>This is the dialog description.</p>

		<button on:click={() => (isOpen = false)}>Close</button>
	</div>
</Dialog>

<style>
	:global(.dialog) {
		position: fixed;
		z-index: 100;
		inset: 0;
	}

	:global(.dialog-overlay) {
		position: fixed;
		left: 0;
		top: 0;
		min-height: 100vh;
		background-color: rgba(0, 0, 0);
		opacity: 0.3;
		inset: 0;
		/* z-index: 100; */
	}

	:global(.dialog-content) {
		background-color: white;
		margin: auto;
		top: 10vh;
		max-width: 300px;
		position: relative;
		z-index: 200;
		padding: 10px 20px;
	}
</style>
