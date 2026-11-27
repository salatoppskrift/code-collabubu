<script setup lang="ts">
import { ref, computed } from 'vue';

const lokalTall = ref(0);
defineProps<{
    globaltTall: number
}>();
defineEmits<{
    'klikkiPaa': []
}>();

</script>

<template>
    <button @click="$emit('klikkiPaa')">Jeg teller: {{ globaltTall }}</button>
</template>