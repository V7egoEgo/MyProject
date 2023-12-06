<template>
	<button class="btn">{{contetn}}</button>
</template>

<script setup>
import {defineProps, defineEmits} from 'vue';
const props = defineProps
({
		contetn:
	{
		type: String,
		default: '',
	},
})

</script>

<style lang="css">
.btn
{
	border: 1px solid #125925;
	background: none;
	border-radius:5px ;
	padding: 7px;
}
.btn:hover
{
	background: #125925;
	color: #fff;
	cursor: pointer;
}
</style>