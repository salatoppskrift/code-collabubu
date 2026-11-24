<script setup lang="ts">
defineProps<{
    tall: number
}>();
const emit = defineEmits<{
    'increaseBy': [val: number]
}>();
</script>

<template>
    <div>
        <p>
        </p>
        <button @click="$emit('increaseBy', 5)">
            {{ tall }}
            Legg til 5 I guess
        </button>
    </div>
</template>