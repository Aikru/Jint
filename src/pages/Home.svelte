<script>
import Header from "../components/Header.svelte";

</script>
<style>
	.triangle {
		clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
		background-color: red;
		width: 35em;
		height: 30em;
		margin: -5%;
		transform: rotate(-10deg);
	}
	.back {
		z-index: -10;
	}
</style>

<div class="App">

	<div class="relative h-screen header">
		
		<Header />
	
		<!-- Typo -->
		<div class="text-6xl text-center text-white rat">
			<p>"une <span class="text-blue-500">party</span> de plaisir"</p>
		</div>
	
	
		<div class="flex justify-center">
			<button class="button-el">Ma soirée</button>
			<button class="button-el">Votre soirée</button>
			<a href="/quizz" class="button-el">Ma soirée parfaite</a>
		</div>
		<img class="absolute top-0 w-full h-full back" src="https://cdn.discordapp.com/attachments/756909801077735518/758258224838737940/Capture_decran_2020-09-23_a_11.27.12.png">
	</div>
	<!--Nav bar-->

	<div class="bg-white">
		<div class="w-1/3 h-20 px-20 my-5 text-4xl text-white bg-red-500 rounded-full rounded-l-none rat align-text text">
			<p>Creer ta soirée</p>
		</div>
	
	
		<div class="flex w-full m-20 flex-raw">
	
			<div class="w-1/4 mx-20 text-4xl text-center text-violet-500 m-50 pop">
				<p>A ton domicile</p>
	
				<p class="w-full text-xl">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
				<button class="w-1/3 text-lg text-red-800 bg-yellow-600 rounded-lg cursor-pointer"> en savoir plus</button>
	
			</div>
	
			
			<div class="w-1/4 mx-20 text-4xl text-center text-violet-500 pop">
				<p>Loue une salle</p>
	
				<p class="w-full text-xl">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
	
				<button class="w-1/3 text-lg text-red-800 bg-yellow-600 rounded-lg cursor-pointer"> en savoir plus</button>
			</div>
	
		</div>
		<div class="w-full h-full bg-red-600">
			<div class="right-0 w-1/3 h-20 px-20 my-5 text-4xl text-white bg-red-500 rounded-full rounded-r-none rat align-text text">
				<p>Créer ta soirée</p>
			</div>
		</div>

		<div class="flex flex-col w-full text-white rat h-500px ">
			<div class="flex flex-col w-1/3 mx-auto my-2 text-indigo-900 pop">Nom <input class="border border-indigo-900 pop" type="text"></div>
			<div class="flex flex-col w-1/3 mx-auto my-2 text-indigo-900 pop">Email <input class="border border-indigo-900 pop" type="email"></div>
			<div class="flex flex-col w-1/3 mx-auto my-2 text-indigo-900 pop">Message <textarea class="w-full h-32 my-0 text-black border border-indigo-900 pop" type="text"></textarea></div>
			<button class="w-1/3 m-auto bg-indigo-900 border pop">Envoyer</button>
		</div>

	</div>
</div>