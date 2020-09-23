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

<div class="flex flex-col w-56 h-56 m-8 border border-white cursor-pointer" on:click={answerSelected}> 
    <div class="w-48 h-48 m-auto bg-white">
        <img class="w-full h-full" src="{answer.image}" alt="Default image">
    </div> 
    <div class="m-auto text-white rat">
        <h1>{answer.label}</h1>
    </div> 
</div>