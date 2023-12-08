<template>
	<div class="input-box">
		<input :type="type" :placeholder="placeholder">
		<p>{{placeholder}}</p>
	</div>
</template>

<script setup>
import {defineProps, defineEmits} from 'vue';
const props = defineProps
({
	type:
	{
		type: [String, Number],
		default: '',
	},
	placeholder:
	{
		type: String,
		default: '',
	},

})


</script>

<style lang="scss">
	.input-box >input
	{
		width: calc(100% - 20px);
		padding: 10px;
		background-color: transparent;
		border-radius: 5px;
		border:1px solid #125925;
		outline : none;

		&:hover + p
		{
			top: -25px;
			left: 10px;
			z-index: 1;
			background-color: #fff;
			opacity: 1;
		}
	}
	.input-box
	{
		position: relative;
		margin-bottom: 10px;
	}
	.input-box > p
	{
		opacity: 0;
		transition: all  .5s;
		position: absolute;
		z-index: -1;
		top: -7px;
		left: 10px;
	}

</style>