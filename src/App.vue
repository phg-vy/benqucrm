<script setup>
import blogCard from './components/blogCard.vue';
import sideBar from './components/sideBar.vue';


</script>

<template>
  <div class=" h-screen p-4 flex gap-8 ">

    <sideBar class="flex-1"></sideBar>

    <div class=" flex-5 rounded-2xl ">
      <div class="flex flex-col gap-8">
        <div class="flex justify-between">
          <h1 class="text-3xl font-semibold ">Blog</h1>
          <iconButton></iconButton>
        </div>
  
        <blogCard></blogCard>

      </div>
    </div>

  </div>
</template>

<style scoped></style>
