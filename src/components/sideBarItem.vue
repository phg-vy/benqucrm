<script setup>
import { ref } from "vue";
const hoveredIndex = ref(null);

const sideBarList = ref([
    { id: 1, name: "Blog", icon: "/icon/blogDefault.svg", hover: "/icon/blogPressed.svg" },
    { id: 2, name: "Category ", icon: "/icon/cateDefault.svg", hover: "/icon/catePressed.svg" },
    { id: 3, name: "Tag", icon: "/icon/tagDefault.svg", hover: "/icon/tagPressed.svg" },
]);

</script>
<template>
    <div v-for="(sideBarItem, index) in sideBarList" :key="sideBarItem.id" class="group flex gap-2 "
        @mouseenter="hoveredIndex = index" @mouseleave="hoveredIndex = null">
        <div
            class="w-full flex p-3 ml-3 rounded-xl gap-3 font-semibold cursor-pointer text-gray-500 hover:bg-blue-100 hover:text-blue-500 active:bg-blue-200">

            <img :src="hoveredIndex === index ? sideBarItem.hover : sideBarItem.icon" alt="">
            <h3 class="w-full"> {{ sideBarItem.name }} </h3>

        </div>

        <div class="h-full w-1 rounded-full group-hover:bg-blue-500 group-active:bg-blue-500"></div>
    </div>
</template>