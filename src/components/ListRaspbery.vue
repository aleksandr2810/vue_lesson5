<template>
	<div class="content">
		<card-raspbery class="element" v-for="card in listData" :key="card.id" :card-data="card" />
	</div>
</template>

<script>
import CardRaspbery from './CardRaspbery.vue';

export default {
	name: 'ListRaspbery',
	components: { CardRaspbery },
	props: {
		listData: {
			type: Array,
			default: () => [],
		}
	},
}
</script>

<style lang="css" scoped>
.content {
	display: flex;
	justify-content: center;
}
.element {
	background-color: yellowgreen;
	padding: 5px;
}
</style>