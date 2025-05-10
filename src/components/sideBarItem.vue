<script setup>
import { ref } from "vue";
const sideBarList = ref([{id:1,name:"Blog",icon:"/icon/blogDefault.svg"},{id:2,name:"Category ",icon:"/icon/cateDefault.svg"},{id:3,name:"Tag",icon:"/icon/tagDefault.svg"}]);

</script>
<template>
    <div v-for="sideBarItem in sideBarList" class="flex p-3 rounded-xl gap-3 font-semibold text-gray-500">
        <img :src="sideBarItem.icon" alt="">
        <h3> {{ sideBarItem.name }} </h3>
    </div>
</template>