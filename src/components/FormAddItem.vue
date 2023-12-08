<template>
	<form class="home-page__form" @submit.prevent>
		<MyInput
			:type = "componetUI.text"
			:placeholder = "componetUI.firstPlaceholder"
		/>
		<MyInput
			:type = "componetUI.text"
			:placeholder = "componetUI.secPlaceholder"
			v-model = "post.name"
		/>
		<MyButton
			:contetn = "componetUI.add"
			@click = "addItem(post)"
		/>
	</form>
</template>

<script setup>
import { ref } from 'vue';
import MyButton from '@/UI/MyButton.vue';
import MyInput from '@/UI/MyInput.vue';

import {defineProps, defineEmits} from 'vue';

const emits = defineEmits(['elemUpdate']);
const componetUI =
{
	add:'добавить',
	firstPlaceholder:'Название',
	secPlaceholder:'Описание',
	text:'text',
}
const post =
{
	id:Math.floor(Math.random() * +Date.now()),
	title:'Заголовок 2',
	change: ref(true),
	body: ref('12412421'),
}

function addItem(elem)
{
	emits('addItem', elem )
}
</script>

<style lang='css'>
	.home-page__form
	{
		width: 100%;
		display: flex;
		justify-content: center;
		flex-direction: column;
		gap: 10px;
		margin: 20px auto;
	}
</style>