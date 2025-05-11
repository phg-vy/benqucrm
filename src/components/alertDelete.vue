<script setup>
import fillButton from '/src/components/fillButton.vue';
const emit = defineEmits(['close']);

</script>
<template>
    <div @click="emit('close')" class="absolute left-1/2 top-1/2 transform -translate-x-1/2 -translate-y-1/2 h-full w-full bg-black/50">
        <div class="z-100 absolute left-1/2 top-1/2 transform -translate-x-1/2 -translate-y-1/2 p-10 text-center gap-x-10 bg-white rounded-xl">
            <h1 class="text-lg pb-3 font-semibold ">Delete Blog</h1>
            <img src="/icon/illustration.svg" alt="" class="py-3">
            <p class="p-3">Are you sure you want to delete this blog?</p>
            <div class="flex place-content-center pt-3 gap-3">

                <fillButton label="Cancel" @click="emit('close')" class="bg-gray-400 shadow-gray-300/50 hover:bg-gray-500 hover:shadow-gray-400/50  active:bg-gray-600" ></fillButton>
                <fillButton label="Delete" ></fillButton>

            </div>
    
        </div>

    </div>
</template>