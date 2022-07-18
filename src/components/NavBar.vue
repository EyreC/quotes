<script setup>
import { ref } from 'vue';
import { reactive } from 'vue';

const state = reactive({ showMenu: true });
// let showMenu = ref(true);
const toggleMenu = () => (state.showMenu = !state.showMenu);
// const toggleMenu = () => console.log('toggling');
defineProps({});
</script>

<template>
	<div>
		<nav
			class="
          flex flex-wrap
          items-center
          justify-between
          w-full
          py-4
          md:py-0
          px-4
          text-lg text-gray-700
          bg-white
        "
		>
			<div>
				<a href="#">
					<!-- Logo goes here -->
					<h1>Words</h1>
				</a>
			</div>

			<svg
				@click="toggleMenu"
				xmlns="http://www.w3.org/2000/svg"
				id="menu-button"
				class="h-6 w-6 cursor-pointer md:hidden block"
				fill="none"
				viewBox="0 0 24 24"
				stroke="currentColor"
			>
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					stroke-width="2"
					d="M4 6h16M4 12h16M4 18h16"
				/>
			</svg>

			<div
				class="w-full md:flex md:items-center md:w-auto"
				:class="{ hidden: state.showMenu }"
				id="menu"
			>
				<ul
					class="
              pt-4
              text-base text-gray-700
              md:flex
              md:justify-between 
              md:pt-0"
				>
					<li>
						<a class="md:p-4 py-2 block hover:text-purple-400" href="#"
							>All Words</a
						>
					</li>
					<li>
						<a class="md:p-4 py-2 block hover:text-purple-400" href="#"
							>Word of the Day</a
						>
					</li>
					<li>
						<a class="md:p-4 py-2 block hover:text-purple-400" href="#"
							>Contribute</a
						>
					</li>
				</ul>
			</div>
		</nav>
	</div>
</template>

<style scoped>
a {
}
</style>
