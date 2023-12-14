<template>
	<form class="home-page__form" @submit.prevent>
	<div class="input-box">
		<input
			v-model="title"
			placeholder="Название">
		<span>
			{{componetUI.firstPlaceholder}}
		</span>

	</div>
	<div class="input-box">
		<input
			v-model="body"
			placeholder="Описание">
		<span>
			{{componetUI.secPlaceholder}}
		</span>
		{{title}}
		 {{body}}
	</div>
		<MyButton
			:contetn = "componetUI.add"
			@click = "addItem(title , body)"
		/>
	</form>
</template>

<script setup>
import { ref } from 'vue';
import MyButton from '@/UI/MyButton.vue';
import MyInput from '@/UI/MyInput.vue';

import {defineProps, defineEmits , reactive} from 'vue';

const emits = defineEmits(['elemUpdate']);
const componetUI =
{
	add:'добавить',
	firstPlaceholder:'Название',
	secPlaceholder:'Описание',
	text:'text',
}
let title =ref(null)
let body = ref(null)

function addItem(titleForm , bodyForm)
{
	const post = reactive(
		{
			id:Math.floor(Math.random() * +Date.now()),
			title: titleForm,
			change: ref(true),
			body: bodyForm,
		})
	emits('addItem', post);
	this.title ='';
	this.body ='';
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