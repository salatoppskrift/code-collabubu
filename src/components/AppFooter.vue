<script setup lang="ts">
defineProps<{
    footerText: string
}>();

</script>

<template>
    <footer>
        {{ footerText }}
    </footer>
</template>