<script setup>
import { ref } from 'vue';

defineProps({
	word: String,
	definition: String,
	color: String,
});

const count = ref(0);
</script>

<template>
	<div
		:class="[
			color,
			'text-slate-600',
			'h-1/3',
			'flex',
			'justify-center',
			'items-center',
		]"
	>
		<div class="h-full max-w-[60%] overflow-hidden min-w-[60%]">
			<div class="min-h-[50%] flex items-end justify-left">
				<h1 class="text-6xl text-left">
					{{ word }}
				</h1>
			</div>
			<h1 class="h-1/2 text-justify">{{ definition }}</h1>
		</div>
	</div>
</template>

<style scoped>
a {
	color: #42b983;
}
</style>
