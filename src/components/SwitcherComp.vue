<script setup>
import { poem } from '../data-poem/poem';
import { ref } from 'vue';

const countShowedQuatrain = ref(poem.value.length);
const quatrainShow = (quatrainId) => {
	const isShowed = poem.value[quatrainId].isShowed;
	if (isShowed) {
		if (countShowedQuatrain.value > 1) {
			poem.value[quatrainId].isShowed = false;
			--countShowedQuatrain.value;
		}
	} else {
		poem.value[quatrainId].isShowed = true;
		++countShowedQuatrain.value;
	}
};
</script>

<template>
	<menu class="switchers">
		<li
			v-for="quatrain of poem"
			:key="quatrain.id"
			class="switchers__quatrain"
			@click="quatrainShow(quatrain.id)"
			:class="
				quatrain.isShowed
					? 'switchers__quatrain--show'
					: 'switchers__quatrain--show-not'
			"
		></li>
	</menu>
</template>

<style scoped lang="scss">
.switchers {
	display: flex;
	gap: 2.25rem;
	padding-top: 6.75rem;
	&__quatrain {
		width: 2.25rem;
		height: 2.25rem;
		border: 0.15rem solid black;
		list-style: none;
		cursor: pointer;
		transition: background-color 0.3s ease-in-out;
		&:hover {
			background-color: #888;
		}
		&--show {
			background-color: black;
			&-not {
				background-color: transparent;
			}
		}
	}
}
</style>
