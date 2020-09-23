<script>

    import AnswerCard from '../components/AnswerCard.svelte';
    import questionsList from '../questions.json';

    let currentQuestion = 0;

    const result = { a: 0, b: 0, c: 0 };

    const questions = shuffle(questionsList);

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
            <h1 class="w-full text-xl text-center text-white rat">Question {currentQuestion + 1} / {questions.length}</h1>
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

