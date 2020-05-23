<template>
	<div class="mt-4 mx-2">
		<!-- Image Cover -->
		<div>
			<a href="#"
				><img
					class="h-30 w-30"
					:src="require(`@/assets/${content.img}`)"
					alt="Album Cover"
			/></a>
		</div>

		<!-- Description -->
		<div>
			<a
				href="#"
				class="hover:text-white hover:underline text-sm text-gray-500 mt-1 font-bold"
				>{{ content.title }}
			</a>
			<p class="text-sm text-gray-500 mt-1">{{ content.description }}</p>
			<p class="text-xs text-gray-500 mt-1 tracking-widest">{{ content.followers }}</p>
		</div>
	</div>
</template>

<script>
export default {
	props: ['content'],
};
</script>
