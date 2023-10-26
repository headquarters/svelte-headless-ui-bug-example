<script>
	import MenuExample from '$lib/MenuExample.svelte';
	import DialogExample from '$lib/DialogExample.svelte';
</script>

<h1>Svelte Headless UI Bug Example</h1>

<p>Standalone dialog example component, only opens when button is pressed.</p>
<DialogExample />

<p>
	Menu with button in it that triggers a dialog when pressed. <em>Bug:</em> The dialog opens as soon
	as the menu opens.
</p>
<MenuExample />
