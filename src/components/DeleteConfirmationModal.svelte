<script lang="ts">
	import { createEventDispatcher } from 'svelte';
	import Modal from './Modal.svelte';

      export let deleteConfirmation: boolean = false;

	const dispatch = createEventDispatcher();
	const closeModal = () => {
		dispatch('close');
	};

	export let isOpen: boolean;
</script>

<Modal {isOpen} on:close={closeModal}>
	<div slot="header" class="card-header flex justify-between items-start">
		<div class="flex flex-col">TIME FOR DELETE</div>
        <button on:click={() => {deleteConfirmation = true}}>Delete</button>
 
	</div></Modal
>
