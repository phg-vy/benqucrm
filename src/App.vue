<script setup>
import sideBar from "./components/sideBar.vue";
import iconTextButton from "./components/iconTextButton.vue";
import blog from "./components/blog.vue";
import Category from "./components/Category.vue";
import alertDelete from "./components/alertDelete.vue";
import tagCreate from "./components/tagCreate.vue"


</script>

<template>
  <!-- <alertDelete></alertDelete> -->

  <div class="h-screen p-4 flex gap-8">
    <sideBar class=" flex-1"></sideBar>
    <div class="flex-5 rounded-2xl">

      <div class="flex flex-col gap-8">
        <!-- <blog></blog> -->
        <!-- <Category></Category>  -->
        <tagCreate></tagCreate>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
