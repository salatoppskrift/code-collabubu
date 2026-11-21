<script setup lang="ts">
defineProps<{ userName: string }>()
const emit = defineEmits<{ 'update:userName': [value: string] }>()
</script>

<template>
  <header>
    <h1>Single lady Code Collab, {{ userName }}</h1>
    <input
      :value="userName"
      @input="emit('update:userName', ($event.target as HTMLInputElement).value)"
      placeholder="Skriv navnet ditt..."
    />
  </header>
</template>