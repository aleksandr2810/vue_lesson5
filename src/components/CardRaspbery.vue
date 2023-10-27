<template>
	<div class="container">
		<div class="images">
			<img class="image" :src="cardData.imgSrc">
		</div>
		<div>
			<img :src="cardData.logo">
			{{ cardData.companyTitle }}
			<span class="in-stoke" v-if="isVisible"> В наличии </span>
			<span  v-else> В пути </span>
		</div>
		<div>
			{{ cardData.description }}
		</div>
	</div>
</template>

<script>
export default {
	name: "CardRaspbery",
	props: {
		cardData: {
			type: Object,
			default: () => ({}),
		}
	},
	// data() {
	// 	return {
	// 		cardData,
	// 	}
	// },
	computed: {
		isVisible() {
			return this.cardData.isInStock
		}
	},
}
</script>

<style lang="css" scoped>
.container {
	width: 145px;
	height: 150px;
}

.in-stoke {
	color: green;
}

.images {
	width: 145px;
	height: 100px;
	text-align: center;
}

.image {
	width: 145px;
	height: 100px;
}
</style>