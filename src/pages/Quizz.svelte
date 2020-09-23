<script>

    import AnswerCard from '../components/AnswerCard.svelte';

    let currentQuestion = 0;

    const result = {
        a: 0,
        b: 0,
        c: 0
    };

    const questions = [{
        title: 'Combien de personnes seront à votre fête ?',
        answers: [
            {
                label: '2 - 10',
                value: 'a'
            },
            {
                label: '11 - 30',
                value: 'b'
            },
            {
                label: '+ 30',
                value: 'c'
            }
        ]
    }].map(question => {
        return {
            ...question,
            answers: shuffle(question.answers)
        }
    });

    function shuffle(a) {
        for (let i = a.length - 1; i > 0; i--) {
            const j = Math.floor(Math.random() * (i + 1));
            [a[i], a[j]] = [a[j], a[i]];
        }
        return a;
    }

    async function addPoints({ detail: answer }) {
        result[answer.value] ++;
        currentQuestion ++;
    }

</script>

<style>
    h1 {
        color: white;
    }
</style>

{#if questions[currentQuestion]}
    <div class="flex flex-col items-center justify-center h-full">
        <div class="w-full text-xl text-center text-white rat">
            <h1>{questions[currentQuestion].title}</h1>
        </div>
        <div class="flex mx-auto">
            <div class="flex mx-auto"> 
                {#each questions[currentQuestion].answers as answer}
                    <AnswerCard answer={answer} on:answerSelected={addPoints} />
                {/each}
            </div>
        </div>
    </div>
{/if}

