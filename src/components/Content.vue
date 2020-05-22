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
		<div class="overflow-y-auto p-4">
			CONTENT
		</div>
	</div>
</template>

<script>
export default {};
</script>
