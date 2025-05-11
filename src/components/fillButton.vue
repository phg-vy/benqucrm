<script setup>
defineProps({
    label: {
        type: String,
        required: true,
    },
});
</script>
<template>
    <button
        class="px-5 h-10 rounded-xl cursor-pointer bg-blue-500 text-white shadow-lg shadow-blue-500/30 hover:bg-blue-600 hover:shadow-blue-500/50 active:bg-blue-700 active:shadow-none">
        {{ label }}

    </button>
</template>