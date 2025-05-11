<script setup>
import iconButton from '/src/components/iconButton.vue';
import iconTextButton from '/src/components/iconTextButton.vue';

import { ref, onMounted } from "vue";
const tagList = ref([
  { id: 1, name: "Business" },
  { id: 2, name: "Education" },
  { id: 3, name: "Fashion" },
]);

import alertDelete from '/src/components/alertDelete.vue';

const showAlert = ref(false); // kiểm soát hiển thị


</script>

<template>
  <div class="flex justify-between pt-6">
    <h1 class="text-3xl font-semibold">Tag</h1>
    <iconTextButton label="Create blog"></iconTextButton>
  </div>
  <div class="flex flex-col gap-4">

    <div v-for="tag in tagList" :key="tag.id" class="flex gap-4 px-4 py-8 bg-white rounded-xl">

      <div class="flex flex-col flex-2 gap-4 text-center">
        <h2 class="text-gray-300">Tag name</h2>
        <p class="justify-between">
          {{ tag.name }}
        </p>
      </div>
      <div class="flex items-center">
        <iconButton @click="showAlert = true"></iconButton>
      </div>
    </div>
  </div>

  <alertDelete v-if="showAlert" @close="showAlert = false" />

</template>
