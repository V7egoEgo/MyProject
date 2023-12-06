<template>
  <div class="conteiner">
    <FormAddItem/>
    <BoxItems :items = "Items"/>
  </div>
</template>

<script setup>
import FormAddItem from '@/components/FormAddItem.vue';
import BoxItems from '@/components/BoxItems.vue';
const Items =
[
  {
    id:1,
    title:"Заголовок 1",
    body: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Necessitatibus excepturi magnam nemo distinctio cupiditate, error sapiente, quibusdam officia quidem ipsam ut ad vel vitae molestias hic? Cupiditate cum dolores, doloribus."
  },
  {
    id:2,
    title:"Заголовок 2",
    body: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Necessitatibus excepturi magnam nemo distinctio cupiditate, error sapiente, quibusdam officia quidem ipsam ut ad vel vitae molestias hic? Cupiditate cum dolores, doloribus."
  },
  {
    id:3,
    title:"Заголовок 3",
    body: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Necessitatibus excepturi magnam nemo distinctio cupiditate, error sapiente, quibusdam officia quidem ipsam ut ad vel vitae molestias hic? Cupiditate cum dolores, doloribus."
  },
  {
    id:4,
    title:"Заголовок 4",
    body: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Necessitatibus excepturi magnam nemo distinctio cupiditate, error sapiente, quibusdam officia quidem ipsam ut ad vel vitae molestias hic? Cupiditate cum dolores, doloribus."
  },
  {
    id:5,
    title:"Заголовок 5",
    body: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Necessitatibus excepturi magnam nemo distinctio cupiditate, error sapiente, quibusdam officia quidem ipsam ut ad vel vitae molestias hic? Cupiditate cum dolores, doloribus."
  },
  {
    id:5,
    title:"Заголовок 6",
    body: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Necessitatibus excepturi magnam nemo distinctio cupiditate, error sapiente, quibusdam officia quidem ipsam ut ad vel vitae molestias hic? Cupiditate cum dolores, doloribus."
  },

]


</script>

<style  lang="scss">

</style>
