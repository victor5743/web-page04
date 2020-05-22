<template>
	<div class="flex-none h-16 px-4 flex items-center justify-between">
		<!-- Song section -->
		<div class="flex items-center">
			<a href="#"><img class="h-12 w-12" src="../assets/cover.jpg" alt="cover image"/></a>
			<div class="ml-3">
				<div class="flex items-center">
					<span>Shape of You</span>
					<a href="#"
						><svg
							class="h-4 w-4 ml-2 text-gray-500 fill-current hover:text-white focus:text-green-700"
							viewBox="0 -28 512.001 512"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M256 455.516c-7.29 0-14.316-2.641-19.793-7.438-20.684-18.086-40.625-35.082-58.219-50.074l-.09-.078c-51.582-43.957-96.125-81.918-127.117-119.313C16.137 236.81 0 197.172 0 153.871c0-42.07 14.426-80.883 40.617-109.293C67.121 15.832 103.488 0 143.031 0c29.555 0 56.621 9.344 80.446 27.77C235.5 37.07 246.398 48.453 256 61.73c9.605-13.277 20.5-24.66 32.527-33.96C312.352 9.344 339.418 0 368.973 0c39.539 0 75.91 15.832 102.414 44.578C497.578 72.988 512 111.801 512 153.871c0 43.3-16.133 82.938-50.777 124.738-30.993 37.399-75.532 75.356-127.106 119.309-17.625 15.016-37.597 32.039-58.328 50.168a30.046 30.046 0 01-19.789 7.43zM143.031 29.992c-31.066 0-59.605 12.399-80.367 34.914-21.07 22.856-32.676 54.45-32.676 88.965 0 36.418 13.535 68.988 43.883 105.606 29.332 35.394 72.961 72.574 123.477 115.625l.093.078c17.66 15.05 37.68 32.113 58.516 50.332 20.961-18.254 41.012-35.344 58.707-50.418 50.512-43.051 94.137-80.223 123.469-115.617 30.344-36.618 43.879-69.188 43.879-105.606 0-34.516-11.606-66.11-32.676-88.965-20.758-22.515-49.3-34.914-80.363-34.914-22.758 0-43.653 7.235-62.102 21.5-16.441 12.719-27.894 28.797-34.61 40.047-3.452 5.785-9.53 9.238-16.261 9.238s-12.809-3.453-16.262-9.238c-6.71-11.25-18.164-27.328-34.61-40.047-18.448-14.265-39.343-21.5-62.097-21.5zm0 0"
							/></svg
					></a>
				</div>
				<a
					href="#"
					class="text-xs text-gray-500 hover:underline hover:text-white focus:text-green-700"
					>Ed Sheeran</a
				>
			</div>
		</div>
		<!-- Player section -->
		<div class=" flex flex-col">
			<div class="flex justify-center">
				<button
					@click="random = !random"
					class="focus:outline-none  relative"
					:class="{
						'text-gray-500': !random,
						'text-green-700': random,
						'hover:text-white': !random,
						'hover:text-green-500': random,
					}"
				>
					<svg
						class="w-4 h-4 fill-current mr-2 mb-1"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
					>
						<path
							d="M6.59 12.83L4.4 15c-.58.58-1.59 1-2.4 1H0v-2h2c.29 0 .8-.2 1-.41l2.17-2.18 1.42 1.42zM16 4V1l4 4-4 4V6h-2c-.29 0-.8.2-1 .41l-2.17 2.18L9.4 7.17 11.6 5c.58-.58 1.59-1 2.41-1h2zm0 10v-3l4 4-4 4v-3h-2c-.82 0-1.83-.42-2.41-1l-8.6-8.59C2.8 6.21 2.3 6 2 6H0V4h2c.82 0 1.83.42 2.41 1l8.6 8.59c.2.2.7.41.99.41h2z"
						/>
					</svg>
					<div
						v-if="random"
						class="w-1 h-1 bg-green-700 rounded-full justify-center ml-1 absolute"
					></div>
				</button>
				<button
					class="focus:outline-none text-gray-500 hover:text-white focus:text-white"
				>
					<svg
						class="w-4 h-4 fill-current mx-2 mb-1"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
					>
						<path d="M4 5h3v10H4V5zm12 0v10l-9-5 9-5z" />
					</svg>
				</button>
				<button
					@click="isOpen = !isOpen"
					class="focus:outline-none text-gray-500 hover:text-white focus:text-white"
				>
					<svg
						v-if="!isOpen"
						class="w-8 h-8 fill-current mx-2 mb-1"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
					>
						<path
							d="M2.93 17.07A10 10 0 1 1 17.07 2.93 10 10 0 0 1 2.93 17.07zm12.73-1.41A8 8 0 1 0 4.34 4.34a8 8 0 0 0 11.32 11.32zM7 6l8 4-8 4V6z"
						/>
					</svg>
					<svg
						v-if="isOpen"
						class="w-8 h-8 fill-current mx-2 mb-1"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
					>
						<path
							d="M2.93 17.07A10 10 0 1 1 17.07 2.93 10 10 0 0 1 2.93 17.07zm12.73-1.41A8 8 0 1 0 4.34 4.34a8 8 0 0 0 11.32 11.32zM7 6h2v8H7V6zm4 0h2v8h-2V6z"
						/>
					</svg>
				</button>
				<button
					class="focus:outline-none text-gray-500 hover:text-white focus:text-white"
				>
					<svg
						class="w-4 h-4 fill-current mx-2 mb-1"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
					>
						<path d="M13 5h3v10h-3V5zM4 5l9 5-9 5V5z" />
					</svg>
				</button>
				<button
					@click="repeat = !repeat"
					class="focus:outline-none relative"
					:class="{
						'text-gray-500': !repeat,
						'text-green-700': repeat,
						'hover:text-white': !repeat,
						'hover:text-green-500': repeat,
					}"
				>
					<svg
						class="w-4 h-4 fill-current mx-2"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
					>
						<path
							d="M10 3v2a5 5 0 0 0-3.54 8.54l-1.41 1.41A7 7 0 0 1 10 3zm4.95 2.05A7 7 0 0 1 10 17v-2a5 5 0 0 0 3.54-8.54l1.41-1.41zM10 20l-4-4 4-4v8zm0-12V0l4 4-4 4z"
						/>
					</svg>
					<div
						v-if="repeat"
						class="w-1 h-1 bg-green-700 rounded-full justify-center ml-4 mt-1 absolute"
					></div>
				</button>
			</div>
			<!-- Music bar -->
			<div class="flex items-center justify-center ml-2">
				<span class="text-xs text-gray-500">1:20</span>
				<div
					class="bg-gray-500 rounded w-112 h-1 mx-2 hover:bg-white cursor-pointer"
				></div>
				<span class="text-xs text-gray-500">3:20</span>
			</div>
		</div>
		<!-- Volume section -->
		<div class="text-gray-500 text-right flex items-center mr-2">
			<svg
				class="fill-current h-4 w-4 hover:text-white cursor-pointer"
				xmlns="http://www.w3.org/2000/svg"
				viewBox="0 0 20 20"
			>
				<path
					d="M17 6V5h-2V2H3v14h5v4h3.25H11a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6zm-5.75 14H3a2 2 0 0 1-2-2V2c0-1.1.9-2 2-2h12a2 2 0 0 1 2 2v4a2 2 0 0 1 2 2v10a2 2 0 0 1-2 2h-5.75zM11 8v8h6V8h-6zm3 11a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"
				/>
			</svg>
			<svg
				class="fill-current h-4 w-4 mx-2 hover:text-white cursor-pointer"
				xmlns="http://www.w3.org/2000/svg"
				viewBox="0 0 20 20"
			>
				<path
					d="M16 17a3 3 0 0 1-3 3h-2a3 3 0 0 1 0-6h2a3 3 0 0 1 1 .17V1l6-1v4l-4 .67V17zM0 3h12v2H0V3zm0 4h12v2H0V7zm0 4h12v2H0v-2zm0 4h6v2H0v-2z"
				/>
			</svg>
			<svg
				class="fill-current h-4 w-4 hover:text-white cursor-pointer"
				xmlns="http://www.w3.org/2000/svg"
				viewBox="0 0 20 20"
			>
				<path
					d="M5 7H1v6h4l5 5V2L5 7zm11.36 9.36l-1.41-1.41a6.98 6.98 0 0 0 0-9.9l1.41-1.41a8.97 8.97 0 0 1 0 12.72zm-2.82-2.82l-1.42-1.42a3 3 0 0 0 0-4.24l1.42-1.42a4.98 4.98 0 0 1 0 7.08z"
				/>
			</svg>
			<div class="bg-gray-500 rounded w-12 h-1 mx-2 hover:bg-white cursor-pointer"></div>
			<svg
				class="fill-current h-4 w-4 hover:text-white cursor-pointer"
				xmlns="http://www.w3.org/2000/svg"
				viewBox="0 0 20 20"
			>
				<path
					d="M2.8 15.8L0 13v7h7l-2.8-2.8 4.34-4.32-1.42-1.42L2.8 15.8zM17.2 4.2L20 7V0h-7l2.8 2.8-4.34 4.32 1.42 1.42L17.2 4.2zm-1.4 13L13 20h7v-7l-2.8 2.8-4.32-4.34-1.42 1.42 4.33 4.33zM4.2 2.8L7 0H0v7l2.8-2.8 4.32 4.34 1.42-1.42L4.2 2.8z"
				/>
			</svg>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			isOpen: false,
			random: false,
			repeat: false,
		};
	},
};
</script>
