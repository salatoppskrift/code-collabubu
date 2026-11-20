<script setup lang="ts">
defineProps<{
    myInputText: string
}>();
const emit = defineEmits<{
    updateText: [value: string]
}>();

</script>

<template>
    <div>
        <input type="text" :value="myInputText" @input="onUpdateText, ($event.target as HTMLInputElement).value" placeholder="the singlest of ladies" />
        <p>{{ myInputText }}</p>
    </div>
</template>