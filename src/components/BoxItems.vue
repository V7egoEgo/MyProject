<template>
	<div class="box" v-for="item in items" :key = "item.id">
		<Item :item = "item"/>
	</div>
	<div v-if="!items.length">
		<h2 class="post-content">Список постов Пуст</h2>
	</div>
</template>

<script setup>
import Item from '@/components/Item.vue';

const props = defineProps
({
	items:
	{
		type: Array,
		default: null,
	},
})
</script>

<style lang="css">
	.post-content
	{
		color: red;
	}
</style>