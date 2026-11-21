<script setup lang="ts">
import { ref } from 'vue'
// import AppHeader from './AppHeader.vue'
import AppHeader from './components/AppHeader.vue';

const bruker1 = ref('dlflddflrld!')
</script>

<template>

  <!-- <AppHeader v-model:user-name="bruker1"/> -->
   <AppHeader v-model:user-name="bruker1"/>
</template>
