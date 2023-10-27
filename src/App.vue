<template>
	<list-raspbery :list-data="raspberryList"/>
</template>

<script>
import ListRaspbery from '@/components/ListRaspbery.vue';
import { raspberryList } from './constants/2_data_raspberry'
export default {
	name: 'App',
	components: {
		ListRaspbery
	},
	data() {
		return {
			raspberryList,
		}
	},
}
</script>

<style>
#app {
	font-size: 14px;
}
</style>
