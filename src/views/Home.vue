<script setup>
import { ref } from 'vue';
import QuoteContainer from '../components/QuoteContainer.vue';
import quotes from '../json/quote_data.json';
defineProps({});

const count = ref(0);
</script>

<template>
	<div class="h-full">
		<QuoteContainer :quotes="quotes" />
	</div>
</template>

<style scoped>
a {
	color: #42b983;
}
</style>
