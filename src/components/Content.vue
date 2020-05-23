<template>
	<div class="flex flex-col w-full bg-second">
		<!-- Top Bar Section -->
		<div class="flex items-center justify-between px-4 py-2">
			<!-- First section -->
			<div class="flex items-center text-gray-500">
				<button class="ml-1 hover:text-white">
					<svg
						class="fill-current w-6 h-6"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
					>
						<path
							d="M7.05 9.293L6.343 10 12 15.657l1.414-1.414L9.172 10l4.242-4.243L12 4.343z"
						/>
					</svg>
				</button>
				<button class="ml-1 hover:text-white">
					<svg
						class="fill-current w-6 h-6"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
					>
						<path
							d="M12.95 10.707l.707-.707L8 4.343 6.586 5.757 10.828 10l-4.242 4.243L8 15.657l4.95-4.95z"
						/>
					</svg>
				</button>
				<div class="flex items-center relative">
					<svg
						class="fill-current w-4 h-4 absolute ml-2"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
					>
						<path
							d="M12.9 14.32a8 8 0 1 1 1.41-1.41l5.35 5.33-1.42 1.42-5.33-5.34zM8 14A6 6 0 1 0 8 2a6 6 0 0 0 0 12z"
						/>
					</svg>
					<input
						class="px-4 py-1 pl-8 rounded-full text-gray-800 focus:outline-none text-gray-800"
						type="text"
						placeholder="Search"
					/>
				</div>
			</div>
			<!-- Second section -->
			<div class="flex items-center">
				<button>
					<svg
						class="fill-current w-4 h-4 mr-2 hover:text-white"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
					>
						<path
							d="M5 5a5 5 0 0 1 10 0v2A5 5 0 0 1 5 7V5zM0 16.68A19.9 19.9 0 0 1 10 14c3.64 0 7.06.97 10 2.68V20H0v-3.32z"
						/>
					</svg>
				</button>
				<button class="hover:underline hover:text-white mx-2 text-sm">User Name</button>
				<button>
					<svg
						class="fill-current w-4 h-4 ml-2 hover:text-white"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
					>
						<path
							d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"
						/>
					</svg>
				</button>
			</div>
		</div>
		<!-- Content Section -->
		<div class="overflow-y-auto p-4 mx-4 my-6 spotify-content">
			<h2 class="text-3xl font-semibold text-white">Home</h2>
			<!-- Recently Played Section -->
			<div class="mt-10">
				<h3 class="font-semibold text-sm border-b border-gray-700 pb-2">
					Recently Played
				</h3>
				<!-- Card component -->
				<div class="flex -mx-2">
					<div class="w-1/4" v-for="(item, index) in content" :key="item.id">
						<Card :content="content[index]" />
					</div>
				</div>
			</div>

			<!-- Your heavy rotation -->
			<div class="mt-10">
				<h3 class="font-semibold text-sm border-b border-gray-700 pb-2">
					Your heavy rotation
				</h3>
				<!-- Card component -->
				<div class="flex -mx-2">
					<div class="w-1/4" v-for="(item, index) in content" :key="item.id">
						<Card :content="content[index]" />
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import Card from './Card.vue';

export default {
	data() {
		return {
			content: [
				{
					title: 'Acoustics Pop Covers',
					description: 'Amazing Acoustic Covers',
					followers: '6,811 FOLLOWERS',
					img: 'cover1.jpg',
				},
				{
					title: 'Acoustics Christmas',
					description: 'Christmas Music',
					followers: '292,145 FOLLOWERS',
					img: 'cover2.jpg',
				},
				{
					title: 'Happy Pop Hits',
					description: 'Amazing Pop Hits',
					followers: '21,687 FOLLOWERS',
					img: 'cover3.jpg',
				},
				{
					title: 'Clasical Christmas',
					description: 'Christmas Music',
					followers: '561,149 FOLLOWERS',
					img: 'cover4.jpg',
				},
			],
		};
	},
	components: {
		Card,
	},
};
</script>

<style scoped>
.spotify-content::-webkit-scrollbar {
	width: 8px;
	height: 8px;
}

.spotify-content::-webkit-scrollbar-thumb {
	background: #646464;
	border-radius: 4px;
}

.spotify-content::-webkit-scrollbar-thumb:active {
	background-color: #646464;
}

.spotify-content::-webkit-scrollbar-thumb:hover {
	background: #757575;
	box-shadow: 0 0 2px 1px rgba(0, 0, 0, 0.2);
}

.spotify-content::-webkit-scrollbar-track {
	background: #bababa;
	border-radius: 4px;
}
</style>
