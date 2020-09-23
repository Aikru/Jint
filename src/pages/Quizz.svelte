<script>

    import AnswerCard from '../components/AnswerCard.svelte';

    let currentQuestion = 0;

    const questions = [{
        title: 'Combien de personnes seront à votre fête ?',
        answers: [
            {
                label: '2 - 10',
                value: 1
            },
            {
                label: '11 - 30',
                value: 2
            },
            {
                label: '+ 30',
                value: 3
            }
        ]
    }];

    async function addPoints({ detail: answer }) {
        console.log('Selected:', answer);
        currentQuestion ++;
    }

</script>

<style>
    h1 {
        color: white;
    }
</style>

{#if questions[currentQuestion]}
    <h1>{questions[currentQuestion].title}</h1>
    {#each questions[currentQuestion].answers as answer}
        <AnswerCard answer={answer} on:answerSelected={addPoints} />
    {/each}
{/if}

