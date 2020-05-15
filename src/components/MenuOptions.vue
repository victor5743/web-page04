<template>
	<a class="flex items-center ml-4 mt-4" href="#">
		<span v-html="options.svg"></span>
		<span class="ml-2 mt-1 text-gray-400 hover:text-white">{{ options.title }}</span>
	</a>
</template>

<script>
export default {
	props: {
		options: Object,
	},
};
</script>
