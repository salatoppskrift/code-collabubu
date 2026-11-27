<script setup lang="ts">
defineProps<{
    text: string
}>();
const emit = defineEmits<{
    'update:text': [value: string]
}>()

</script>

<template>
    <article>
        <p>tekstinnhold: {{ text }}</p>
        <!-- <input id="editor" :value="text" @input="$emit('update:text', ($event.target as HTMLInputElement).value)"/> -->

        <textarea name="editor" id="editor" :value="text" @input="$emit('update:text', ($event.target as HTMLTextAreaElement).value)"></textarea>
    </article>
</template>

<style scoped>
  article > textarea {
    width: 80%;
  }
</style>