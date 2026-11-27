<script setup lang="ts">
  import {computed} from 'vue';
  const props = defineProps<{
    initial: number,
    step: number
  }>();
  const emit = defineEmits<{
    'addCount': [value: number],
    'removeCount': []
  }>();

  const doubled = computed(() => {
    return props.step * 2;
  })
</script>

<template>
    <button @click="$emit('addCount', step)"> Trykk for å gjøre større: {{ initial }}</button>
    <button @click="$emit('removeCount')">Fjern fra intiial</button>
    <p>{{ doubled }}</p>
</template>