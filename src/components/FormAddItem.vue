<template>
	<form class="home-page__form">
		<MyInput :type = "text" :placeholder = "firstPlaceholder"/>
		<MyInput :type = "text" :placeholder = "secPlaceholder" />
		<MyButton :contetn = "add"/>
	</form>
</template>

<script setup>
import MyButton from '@/UI/MyButton.vue';
import MyInput from '@/UI/MyInput.vue';
const add = "добавить";
const firstPlaceholder = "Название";
const secPlaceholder = "Описание"
const text = "text";
</script>

<style lang="css">
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