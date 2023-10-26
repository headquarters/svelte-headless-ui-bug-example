<script>
	import { Menu, MenuButton, MenuItems, MenuItem } from '@rgossiaux/svelte-headlessui';
	import DialogExample from './DialogExample.svelte';
</script>

<Menu>
	<MenuButton>Open Menu</MenuButton>
	<MenuItems class="menu-items">
		<MenuItem let:active>
			<DialogExample />
		</MenuItem>
		<MenuItem disabled>
			<span class="disabled">Disabled menu option</span>
		</MenuItem>
	</MenuItems>
</Menu>

<style>
	:global(.menu-items) {
		max-width: 200px;
		background: lightgray;
		padding: 10px 20px;
	}

	:global(.menu-items a) {
		display: block;
		padding: 4px 4px 2px 0;
	}
</style>
