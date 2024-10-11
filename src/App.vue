<script setup>
import HeaderComp from './components/HeaderComp.vue';
import SwitcherComp from './components/SwitcherComp.vue';
import PoemTextComp from './components/PoemTextComp.vue';
</script>

<template>
	<div class="container">
		<SwitcherComp />
		<article>
			<HeaderComp
				:title="`invictus`"
				:author="`by william ernest henley`"
			/>
			<PoemTextComp />
		</article>
	</div>
</template>

<style lang="scss">
.container {
	display: flex;
	flex-wrap: wrap;
	gap: 2.5rem;
}
</style>
