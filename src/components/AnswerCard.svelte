<script>

    import { createEventDispatcher } from 'svelte';

    export let answer;

    const dispatch = createEventDispatcher();

    async function answerSelected() {
        dispatch('answerSelected', answer);
    }

</script>

<style>
    h1 {
        color: white;
    }
</style>

<div on:click={answerSelected}>
    <h1>{answer.label}</h1>
</div>