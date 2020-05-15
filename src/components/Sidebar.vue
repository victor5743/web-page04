<template>
	<div class="w-1/5 flex flex-none flex-col justify-between bg-first">
		<!-- Menu Options -->
		<div>
			<ul class="py-2">
				<li class="mt-4" v-for="(item, index) in options" :key="item.id">
					<MenuOptions :options="options[index]" />
				</li>
			</ul>
		</div>

		<!-- Music Options -->
		<div class="overflow-y-auto">
			<!-- Library -->
			<div class="px-4 mt-2">
				<h3 class="uppercase tracking-widest text-gray-500 text-xs">Your Library</h3>
				<ul class="leading-loose">
					<li v-for="item in library" :key="item.id">
						<a class="hover:text-white" href="#">{{ item.msg }}</a>
					</li>
				</ul>
			</div>

			<!-- Playlists -->
			<div class="px-4 mt-4">
				<h3 class="uppercase tracking-widest text-gray-500 text-xs">Playlists</h3>
				<ul class="leading-loose">
					<li class="truncate" v-for="item in playlists" :key="item.id">
						<a class="hover:text-white" href="#">{{ item.msg }}</a>
					</li>
				</ul>
			</div>
		</div>

		<!-- New Playlist Option -->
		<div class="py-2 border-t border-gray-500">
			<MenuOptions :options="playlist" />
		</div>
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
			library: [
				{ msg: 'Made For You' },
				{ msg: 'Recently Played' },
				{ msg: 'Liked Songs' },
				{ msg: 'Albums' },
				{ msg: 'Artists' },
				{ msg: 'Podcasts' },
			],
			playlists: [
				{ msg: 'Acoustic Hits' },
				{ msg: 'Acoustic Covers' },
				{ msg: 'Discovery Weekly' },
				{ msg: 'Hot Hits Canada' },
				{ msg: "90's Hip-Hop" },
				{ msg: "90's Smash Hits" },
				{ msg: 'TGIF' },
				{ msg: 'Mint Canada' },
				{ msg: 'Hip-Hop Central' },
				{ msg: 'R&B Right Now' },
				{ msg: "I Love My 'OOs R&B" },
				{ msg: "Chris Lake's Dance" },
				{ msg: 'I Love My 90s R&B Hip-Hop' },
				{ msg: 'Are & Be' },
				{ msg: "Today's Top Hits" },
				{ msg: 'Get Turnt' },
				{ msg: 'iTunes' },
			],
			playlist: {
				title: 'New playlist',
				svg:
					'<svg class="fill-current text-white" width="18" height="18" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M12.9 14.32a8 8 0 1 1 1.41-1.41l5.35 5.33-1.42 1.42-5.33-5.34zM8 14A6 6 0 1 0 8 2a6 6 0 0 0 0 12zM7 7V5h2v2h2v2H9v2H7V9H5V7h2z"/></svg>',
			},
		};
	},
	components: {
		MenuOptions,
	},
};
</script>
