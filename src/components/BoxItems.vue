<template>
	<div class="box" v-for="item in items" :key = "item.id">
		<div class="Item-box">
			<div>
				<h2>{{item.title}}</h2>
				<p v-if = "item.change">{{item.body}}</p>
				<div v-else class="input-box">
					<input
						type="text"
						placeholder="изменение текста"
						v-model = "item.body"
						>
					<span>
						изменение текста
					</span>
				</div>
			</div>
			<div class="Item-btn">
				<MyButton
				@click = "myMethod(componetUI.change, item.id , items)"
				:contetn = "componetUI.change" />
				<MyButton
				@click = "myMethod(componetUI.delet ,item.id , items)"
				:contetn = "componetUI.delet"/>
			</div>
		</div>
	</div>
	<div v-if="!items.length">
		<h2 class="post-content">Список постов Пуст</h2>
	</div>
</template>

<script setup>
import MyButton from '@/UI/MyButton.vue';
import MyInput from '@/UI/MyInput.vue';
import {defineProps, defineEmits} from 'vue';


const emits = defineEmits(['elemUpdate']);
const componetUI =
{
	change:'Изменить',
	delet:'Удалить',
	text:'text',
	placeholder: 'изменение текста'
}
const props = defineProps
({
	items:
	{
		type: Array,
		default: null,
	},
})

function myMethod(action , elem)
{
	emits('elemUpdate', elem , action)
}
</script>

<style lang="scss">
	.box
	{
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.Item-btn
	{
		display: flex;
		gap: 20px;
	}
	.Item-box
	{
		width: 100%;
	}
	.Item-box > .input-box
	{
		margin-bottom: 10px;
	}
	.Item-btn > button{width: 15%;}
</style>