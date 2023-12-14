<template>
	<div class="input-box">
		<input
			:modelValue="modelValue"
			@input="$emit('update:modelValue', $event.target.value)"
			:type="type"
			:placeholder="placeholder">
		<span>
			{{placeholder}}
		</span>
		{{modelValue}}
	</div>
</template>

<script setup>
import {defineProps, defineEmits, ref} from 'vue';

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
	modelValue:
	{
		type: String,
		default: '',
	}

})
const emit = defineEmits(['update:modelValue'])
	const inputRef = ref();




function updateValue()
{
	emit('update:modelValue', null);
	nextTick(() => focusOut())
}

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

		&:hover + span
		{
			top: -10px;
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
	.input-box > span
	{
		opacity: 0;
		transition: all  .5s;
		position: absolute;
		z-index: -1;
		top: -7px;
		left: 10px;
	}

</style>