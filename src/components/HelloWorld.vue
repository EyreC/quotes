<script setup>
import { ref } from 'vue';
import QuoteCard from './QuoteCard.vue';
defineProps({
	quotes: Array,
});

const count = ref(0);
</script>

<template>
	<div>
		<QuoteCard
			v-for="quote in quotes"
			:word="quote.word"
			:definition="quote.definition"
			:color="quote.color"
		/>
	</div>
</template>

<style scoped>
a {
	color: #42b983;
}
</style>
