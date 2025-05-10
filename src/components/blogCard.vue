<script setup>
import fillButton from '/src/components/fillButton.vue'
import iconButton from '/src/components/iconButton.vue'

</script>

<template>
    <div class="flex gap-4 px-4 py-8 bg-white rounded-xl ">

        <div class="flex flex-col gap-4 flex-2 text-center align-center">
            <h2 class="text-gray-300">Blog Title</h2>
            <p class="text-justify">Lorem ipsum dolor sit amet consectetur adipiscing elit. Dolor sit amet consectetur adipiscing elit quisque
                faucibus.</p>
        </div>
    
        <div class="flex flex-col gap-4 flex-1 text-center ">
            <h2 class="text-gray-300">Writer</h2>
            <p>JUSTIND</p>
        </div>
    
        <div class="flex flex-col gap-4 flex-1 text-center ">
            <h2 class="text-gray-300">Category</h2>
            <p>Business</p>
        </div>
    
        <div class="flex items-center ">
            <fillButton></fillButton>
        </div>
        <iconButton></iconButton>

    </div>

</template>