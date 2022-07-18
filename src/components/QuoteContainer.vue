<script setup>
import { ref } from 'vue';
import QuoteCard from './QuoteCard.vue';

const colorCount = 4;
const colors = ['bg-red-100', 'bg-stone-300', 'bg-teal-100', 'bg-indigo-100'];
const colorPicker = (currentIdx) => colors[currentIdx % colorCount];

defineProps({
	quotes: Array,
});

const count = ref(0);
</script>

<template>
	<div class="h-full">
		<QuoteCard
			v-for="(quote, idx) in quotes"
			:word="quote.word"
			:definition="quote.definition"
			:color="colorPicker(idx)"
		/>
	</div>
</template>

<style scoped></style>
