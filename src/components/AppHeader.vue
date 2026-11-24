<script setup lang="ts">
defineProps<{
  userName: string,
  userName2: string
}>()
const emit = defineEmits<{
  'update:userName': [value: string],
  'update:userName2': [value: string],
}>();

</script>

<template>
  <header>
    <h1>Single lady Code Collab{{
      userName.trim().length > 0 && userName2.trim().length > 0
        ? ", " + userName.trim() + " og " + userName2.trim() + "!!"
        : [userName.trim(), userName2.trim()].some(name => name.length !== 0)
          ? (", " + [userName.trim(),
          userName2.trim()].filter(name => name.length !== 0)[0]) + "!"
          : ''
    }}</h1>
    <p>
      <label for="bruker1">Bruker#1: </label>
      <input id="bruker1" :value="userName" @input="$emit('update:userName', ($event.target as HTMLInputElement).value)"
        placeholder="Skriv navnet ditt..." />
    </p>
    <p>
      <label for="bruker2">Bruker#2: </label>
      <input id="bruker2" :value="userName2"
        @input="$emit('update:userName2', ($event.target as HTMLInputElement).value)"
        placeholder="Skriv navn til noen andre...">
    </p>
  </header>
</template>