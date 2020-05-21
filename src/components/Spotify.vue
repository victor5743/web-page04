<template>
	<div class="flex flex-col h-screen">
		<div class="bg-blue-500 flex-1 flex overflow-y-hidden">
			<Sidebar />
			<div class="w-full overflow-y-auto bg-second">Content</div>
		</div>
		<div class="bg-third">
			<Bottom />
		</div>
	</div>
</template>

<script>
import Sidebar from './Sidebar.vue';
import Bottom from './Bottom.vue';
// import Content from './Content.vue';

export default {
	components: {
		Sidebar,
		Bottom,
		// Content,
	},
};
</script>
