<script setup lang="ts">
import { ref } from 'vue';

import SingleLadyAppHeader from './components/SingleLadyAppHeader.vue';
import SingleLadyAppFooter from './components/SingleLadyAppFooter.vue';
import SingleLadyAppTextEditor from './components/SingleLadyAppTextEditor.vue';
import SingleLadyAssistantPanel from './components/SingleLadyAssistantPanel.vue';

const whatever = ref('something');

</script>

<template>
  <SingleLadyAppHeader />
  <SingleLadyAppTextEditor v-model:text="whatever"/>
  <SingleLadyAssistantPanel />
  <SingleLadyAppFooter />
</template>
