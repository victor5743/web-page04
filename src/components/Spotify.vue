<template>
	<div class="flex flex-col h-screen">
		<div class="flex-1 flex overflow-y-hidden">
			<Sidebar />
			<Content />
		</div>
		<div class="bg-third">
			<Bottom />
		</div>
	</div>
</template>

<script>
import Sidebar from './Sidebar.vue';
import Bottom from './Bottom.vue';
import Content from './Content.vue';

export default {
	components: {
		Sidebar,
		Bottom,
		Content,
	},
};
</script>
