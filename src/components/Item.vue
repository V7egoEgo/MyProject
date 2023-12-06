<template>
	<div class="Item-box">
		<div>
			<h2>{{item.title}}</h2>
			<p>{{item.body}}</p>
		</div>
		<div class="Item-btn">
			<MyButton class="" :contetn = "btnChangeText" />
			<MyButton :contetn = "btnDeletText"/>
		</div>
	</div>

</template>

<script setup>
import MyButton from '@/UI/MyButton.vue';
const btnChangeText = 'Изменить';
const btnDeletText = 'Удалить';

const props = defineProps
({
	item:
	{
		type: Object,
		default: null,
	},
})
</script>

<style lang="scss" scoped>
	.Item__box
	{
		display: flex;
		align-items: center;
		border: 1px solid green;
		padding: 20px;
		border-radius: 8px;
	}
	.Item-btn
	{
		display: flex;
		gap: 20px;
		justify-content: center;
		button{width: 40%;}
	}
</style>