<script setup>
import fillButton from '/src/components/fillButton.vue';
import iconButton from '/src/components/iconButton.vue';
import iconTextButton from '/src/components/iconTextButton.vue';

import { ref } from "vue";
const blogList = ref([
    { id: 1, title: "Lorem ipsum dolor sit amet consectetur adipiscing elit. Dolor sit amet consectetur adipiscing elit quisque faucibus.", writer: "JUSTIND", cate: "Business" },
    { id: 2, title: "Lorem ipsum dolor sit amet consectetur adipiscing elit.", writer: "JUSTIND", cate: "Education" },
    { id: 3, title: "Lorem ipsum dolor sit amet consectetur adipiscing elit. Dolor sit amet consectetur adipiscing elit quisque faucibus.", writer: "JUSTIND", cate: "Health" },
]);

import alertDelete from '/src/components/alertDelete.vue';

const showAlert = ref(false); // kiểm soát hiển thị

</script>

<template>

    <div class="flex justify-between pt-6">
        <h1 class="text-3xl font-semibold">Blog</h1>
        <iconTextButton label="Create blog"></iconTextButton>
    </div>
    <div class="flex flex-col gap-4">
            <div v-for="blogListItem in blogList" :key="blogListItem.id"
        class="flex gap-3 px-4 py-8 bg-white rounded-xl hover:shadow-lg hover:shadow-blue-300/30">


        <div class="flex flex-col gap-4 flex-2 text-center align-center">
            <h2 class="text-gray-300">Blog Title</h2>
            <p class="line-clamp-2">{{ blogListItem.title }}</p>
        </div>

        <div class="flex flex-col gap-4 flex-1 text-center ">
            <h2 class="text-gray-300">Writer</h2>
            <p>{{ blogListItem.writer }}</p>
        </div>

        <div class="flex flex-col gap-4 flex-1 text-center ">
            <h2 class="text-gray-300">Category</h2>
            <p>{{ blogListItem.cate }}</p>
        </div>

        <div class="flex items-center ">
            <fillButton label="Edit"></fillButton>
        </div>
        <div class="flex items-center">
            <iconButton @click="showAlert = true"></iconButton>
        </div>

    </div>
    <alertDelete v-if="showAlert" @close="showAlert = false" />
    </div>



</template>