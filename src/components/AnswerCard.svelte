<script>

    import { createEventDispatcher } from 'svelte';

    export let answer;

    const dispatch = createEventDispatcher();

    async function answerSelected() {
        dispatch('answerSelected', answer);
    }

</script>

<div class="flex flex-col w-56 h-56 m-8 bg-white border border-white rounded cursor-pointer" on:click={answerSelected}> 
    <div class="w-48 h-48 pt-2 m-auto bg-white">
        <img class="w-full h-full rounded" src="{answer.image}" alt="Default image">
    </div> 
    <div class="m-auto text-white rat">
        <h1 class="text-black">{answer.label}</h1>
    </div> 
</div>