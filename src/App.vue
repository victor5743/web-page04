<template>
	<div class="font-roboto tracking-wide text-gray-400" id="app">
		<Spotify />
	</div>
</template>

<script>
import Spotify from './components/Spotify.vue';

export default {
	name: 'App',
	components: {
		Spotify,
	},
};
</script>

<style src="./assets/css/tailwind.css"></style>
