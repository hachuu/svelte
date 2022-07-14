<script>
	import Header from "./Header.svelte";
	import Modal from "./Modal.svelte";
	let name = 'world';
</script>

<h1>Hello {name}!</h1>
<Header name="header" />
<Modal />