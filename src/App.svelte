<script lang="ts">
	import { sampleCode } from './sampleCode.js';
	
	import Header from './Header.svelte';
	import Editor from './Editor.svelte';
	import Qbutton from './Qbutton.svelte';
	import Previewer from './Previewer.svelte';
	import Modal from './Modal.svelte';

	let markDown: string = sampleCode;
	$: cleanHTML = DOMPurify.sanitize(markDown)
	$: htmlDisplay = marked(cleanHTML, { breaks: true, gfm:true, langPrefix:'language'});

	let modalOpen: boolean = false;
	const handleModal = () => modalOpen = !modalOpen;	
</script>


<Header />
<main>
	<Editor bind:markDown />
	<Qbutton on:click={handleModal} />
	<Previewer {htmlDisplay} />

	<Modal on:click={handleModal} {modalOpen} />
</main>


<style>
	@import url('https://fonts.googleapis.com/css2?family=Delius+Swash+Caps&display=swap');

	main {
		width: 100%;
		padding: 5% 0;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		background-color: #333;
		font-family: Merriweather, serif;
		position: relative;
	}

	/* @media (min-width: 640px) {
		main {
			max-width: none;
		}
	} */
</style>