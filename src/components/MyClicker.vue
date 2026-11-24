<script setup lang="ts">
import { ref, computed } from 'vue';

const lokalTall = ref(0);
defineProps<{
    globaltTall: number
}>();
defineEmits<{
    'klikkiPaa': [val: number]
}>();

</script>

<template>
    <button @click="$emit('klikkiPaa', 5)">Jeg teller: {{ globaltTall }}</button>
</template>