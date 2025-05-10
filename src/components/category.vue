<script setup>
import iconButton from "/src/components/iconButton.vue";
import { ref, onMounted } from "vue";
const cateList = ref([
  { id: 1, name: "Business" },
  { id: 2, name: "Education" },
  { id: 3, name: "Fashion" },
]);
</script>

<template>
  <div v-for="cate in cateList" :key="cate.id" class="flex gap-4 px-4 py-8 bg-white rounded-xl">
    <div class="flex flex-col flex-2 text-center">
      <h2 class="text-gray-300">Category name</h2>
      <p class="justify-between">
        {{ cate.name }}
      </p>
    </div>
    <iconButton></iconButton>
  </div>
</template>
