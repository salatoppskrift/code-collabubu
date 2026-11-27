<script setup lang="ts">
import { ref, computed } from 'vue'
// import AppHeader from './AppHeader.vue'
import AppHeader from './components/AppHeader.vue';
import MyClicker from './components/MyClicker.vue';
import AppTextEditor from './components/AppTextEditor.vue';
import AssistantPanel from './components/AssistantPanel.vue';
import AppFooter from './components/AppFooter.vue';

const bruker1 = ref('');
const bruker2 = ref('');

const tall = ref(0);

const editorText = ref('');
const assistantTitle = ref('Assistentpanel');
const footerText = ref('👣 fot©')

const klikker = () => {
    tall.value++;
};

</script>

<template>

    <!-- <AppHeader v-model:user-name="bruker1"/> -->
    <AppHeader v-model:user-name="bruker1" v-model:user-name2="bruker2" />
    <MyClicker :globalt-tall="tall"/>
    <AppTextEditor v-model:text="editorText"/>
    <AssistantPanel v-model="assistantTitle"/>
    
    <AppFooter :footer-text="footerText"/>
</template>
<style scoped>
.red {
    color: maroon;
}
</style>