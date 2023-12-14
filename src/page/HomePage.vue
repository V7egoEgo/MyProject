<template>
  <div class="conteiner">
    <FormAddItem
    	@addItem ="addItem"
    />
    <BoxItems
				@elemUpdate ="updeteItem"
				:items = "items"
    	/>
  </div>
</template>

<script setup>
import FormAddItem from '@/components/FormAddItem.vue';
import BoxItems from '@/components/BoxItems.vue';
import { ref , reactive } from 'vue';
const items = reactive([
	{
		id:1,
		title:'Заголовок 1',
		change: ref(true),
		body: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Necessitatibus excepturi magnam nemo distinctio cupiditate, error sapiente, quibusdam officia quidem ipsam ut ad vel vitae molestias hic? Cupiditate cum dolores, doloribus.'
	},
	{
		id:2,
		title:'Заголовок 2',
		change: ref(true),
		body: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Necessitatibus excepturi magnam nemo distinctio cupiditate, error sapiente, quibusdam officia quidem ipsam ut ad vel vitae molestias hic? Cupiditate cum dolores, doloribus.'
	},
	{
		id:3,
		title:'Заголовок 3',
		change: ref(true),
		body: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Necessitatibus excepturi magnam nemo distinctio cupiditate, error sapiente, quibusdam officia quidem ipsam ut ad vel vitae molestias hic? Cupiditate cum dolores, doloribus.'
	},
	{
		id:4,
		title:'Заголовок 4',
		change: ref(true),
		body: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Necessitatibus excepturi magnam nemo distinctio cupiditate, error sapiente, quibusdam officia quidem ipsam ut ad vel vitae molestias hic? Cupiditate cum dolores, doloribus.'
	},
	{
		id:5,
		title:'Заголовок 5',
		change: ref(true),
		body: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Necessitatibus excepturi magnam nemo distinctio cupiditate, error sapiente, quibusdam officia quidem ipsam ut ad vel vitae molestias hic? Cupiditate cum dolores, doloribus.'
	},
	{
		id:6,
		title:'Заголовок 6',
		change: ref(true),
		body: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Necessitatibus excepturi magnam nemo distinctio cupiditate, error sapiente, quibusdam officia quidem ipsam ut ad vel vitae molestias hic? Cupiditate cum dolores, doloribus.'
	},
])


function updeteItem( elem, action )
{
	if (action === 'Изменить')
	{
		const findIdx = items.findIndex(el => el.id === elem);
		items[findIdx].change = !items[findIdx].change
	}
	if(action === 'Удалить')
	{
		const findIdx = items.findIndex(el => el.id === elem);
		items.splice(findIdx , 1)
	}
}

function addItem( elem)
{
	items.push( elem )
}

</script>

<style  lang="scss">

</style>
