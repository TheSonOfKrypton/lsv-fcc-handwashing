<script>
	import Timer from './Timer.svelte';
	import HowTo from './HowTo.svelte';
	let audio;

	function endTimer() {
		audio.play();
	}
</script>

<style>
	h1 {
		text-align: center;
	}
</style>

<h1>Handwashing App</h1>

<Timer on:end={endTimer}/>

<HowTo />

<audio bind:this={audio}>
	<source src="public_sound.wav">
</audio>