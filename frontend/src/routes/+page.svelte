<script lang="ts">
	import { Greet } from '$lib/wailsjs/go/app/App';

	let name = 'world';
	let text = 'Please enter your name and click Go!';
</script>

<div class="container h-full mx-auto flex justify-center items-center">
	<div class="space-y-10 text-center flex flex-col items-center">
		<h2 class="h2">Welcome to Skeleton.</h2>
		<!-- Animated Logo -->
		<div class="flex">
			<input class="input" type="text" placeholder="Input" bind:value={name} />
			<button
				class="btn variant-filled"
				on:click={async () => {
					text = await Greet(name);
				}}>Go!</button
			>
		</div>
		<div><h3 class="h3">{text}</h3></div>
	</div>
</div>

<style lang="scss">
</style>
