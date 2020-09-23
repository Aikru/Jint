
<script>
	import { Route } from 'tinro';
	import Home from './pages/Home.svelte';
	import Quizz from './pages/Quizz.svelte';
</script>

<style>
	:global(body) {
		margin: 0;
		font-family: Arial, Helvetica, sans-serif;
		background-color:#2b0b4b;
	}
</style>

<Route path="/"><Home /></Route>
<Route path="/quizz"><Quizz /></Route>

