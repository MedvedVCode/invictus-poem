<script setup>
const props = defineProps({
	title: String,
	author: String,
});
</script>

<template>
	<div class="header">
		<h1 class="header-title">{{ props.title }}</h1>
		<address class="header-author">{{ props.author }}</address>
	</div>
</template>

<style lang="scss">
.header {
	display: flex;
	text-transform: capitalize;
	align-items: baseline;
	flex-wrap: wrap;
	margin-left: 14.125em;
	margin-bottom: 1.6rem;

	&-title {
		font-weight: 500;
		font-size: 4rem;
		line-height: 4.5rem;
		padding-right: 7.5rem;
	}
	&-author {
		font-size: 2rem;
		font-style: normal;
		line-height: 4.5rem;
	}
}
</style>
