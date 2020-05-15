<template>
	<div class="w-1/5 flex flex-none flex-col justify-between bg-first">
		<div>
			<ul class="py-2">
				<li
					class="border-l-4 border-green-600"
					v-for="(item, index) in options"
					:key="item.id"
				>
					<MenuOptions :options="options[index]" />
				</li>
			</ul>
		</div>
		<div class="overflow-y-auto">
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo ducimus accusamus
			deleniti consectetur sit facilis sequi, dignissimos recusandae eligendi minima
			blanditiis animi tempora minus veritatis voluptates ad similique earum. Repellendus?
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo ducimus accusamus
			deleniti consectetur sit facilis sequi, dignissimos recusandae eligendi minima
			blanditiis animi tempora minus veritatis voluptates ad similique earum. Repellendus?
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo ducimus accusamus
			deleniti consectetur sit facilis sequi, dignissimos recusandae eligendi minima
			blanditiis animi tempora minus veritatis voluptates ad similique earum. Repellendus?
		</div>
		<div>Three</div>
	</div>
</template>

<script>
import MenuOptions from './MenuOptions.vue';

export default {
	data() {
		return {
			// Menu Options
			options: [
				{
					title: 'Home',
					svg:
						'<svg class="fill-current text-white" width="18" height="18" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M8 20H3V10H0L10 0l10 10h-3v10h-5v-6H8v6z"/></svg>',
				},
				{
					title: 'Browse',
					svg:
						'<svg class="fill-current text-white" width="18" height="18" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M16 2h4v15a3 3 0 0 1-3 3H3a3 3 0 0 1-3-3V0h16v2zm0 2v13a1 1 0 0 0 1 1 1 1 0 0 0 1-1V4h-2zM2 2v15a1 1 0 0 0 1 1h11.17a2.98 2.98 0 0 1-.17-1V2H2zm2 8h8v2H4v-2zm0 4h8v2H4v-2zM4 4h8v4H4V4z"/></svg>',
				},
				{
					title: 'Radio',
					svg:
						'<svg class="fill-current text-white" width="18" height="18" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M20 9v9a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V8c0-1.1.9-2 2-2h13.8L.74 1.97 1.26.03 20 5.06V9zm-5 9a3 3 0 1 0 0-6 3 3 0 0 0 0 6zM2 8v2h16V8H2zm1.5 10a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3zm5 0a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3zm6.5-1a2 2 0 1 1 0-4 2 2 0 0 1 0 4z"/></svg>',
				},
			],
		};
	},
	components: {
		MenuOptions,
	},
};
</script>
