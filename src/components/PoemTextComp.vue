<script setup>
import { computed } from 'vue';
import { poem } from '../data-poem/poem';

const showPoem = computed(() => {
	return poem.value.filter((item) => item.isShowed);
});
</script>

<template>
	<ul class="poem">
		<li
			class="quatrain"
			v-for="quatrain in showPoem"
			:key="quatrain.id"
		>
			{{ quatrain.quatrainText }}
		</li>
	</ul>
</template>

<style scoped lang="scss">
.poem{
	min-width: 290px;
	width: 100%;
}
.quatrain {
	font-size: 2.5rem;
	line-height: 1.25;
	white-space: pre-wrap;
	margin-bottom: 3rem;
	list-style: none;
	word-spacing: 0.5rem;
	&:last-child {
		margin-bottom: 0;
	}
}
</style>
