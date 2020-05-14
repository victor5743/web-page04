<template>
	<div class="flex flex-col h-screen">
		<div class="bg-blue-500 flex-1 flex overflow-y-hidden">
			<Sidebar />
			<div class="bg-purple-500 w-full overflow-y-auto">Content</div>
		</div>
		<div class="bg-red-500">Bottom</div>
	</div>
</template>

<script>
import Sidebar from './Sidebar.vue';
// import Content from './Content.vue';
// import Bottom from './Bottom.vue';

export default {
	components: {
		Sidebar,
		// Content,
		// Bototom,
	},
};
</script>
