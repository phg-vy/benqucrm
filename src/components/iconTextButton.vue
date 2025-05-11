<script setup>
defineProps({
    label: {
        type: String,
        required: true,
    },
});
</script>
<template>
    <div class=" pl-2 pr-3 py-3 flex gap-2 rounded-xl cursor-pointer bg-blue-500 text-white shadow-lg shadow-blue-500/30 hover:bg-blue-600 hover:shadow-blue-500/50 active:bg-blue-700 active:shadow-none">
        <img src="/icon/plus.svg" alt="">
        {{ label }}
    </div>
</template>