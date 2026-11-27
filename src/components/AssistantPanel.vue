<script setup lang="ts">
const tittel = defineModel<string>({default: 'Foreløpig tittel'});

</script>

<template>
    <h2>{{ tittel }}</h2>
</template>