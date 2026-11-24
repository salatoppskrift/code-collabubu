<script setup lang="ts">
import { ref, computed } from 'vue'
// import AppHeader from './AppHeader.vue'
import AppHeader from './components/AppHeader.vue';
import MyClicker from './components/MyClicker.vue';

const bruker1 = ref('a');
const bruker2 = ref('');

const tall = ref(0);

// function greeting() {
//   const nameLengths = [userName.trim().length, userName2.trim().length];
//   if (nameLengths.every(length => length <= 0)) return '';
//   else if (nameLengths.every(length => length > 0)) return ', ' + userName + " og " userName2 + "!";
//   if (nameLengths.some(length => length > 0)) {
//     let text = "";
//     text += ", ";
//     if (nameLengths[0] > 0 && nameLengths[1] === 0) text += userName;
//     else text += userName2;
//     return text;
//   }
// }

const klikker = computed( () => {
    tall.value++; 
});
</script>

<template>

  <!-- <AppHeader v-model:user-name="bruker1"/> -->
   <AppHeader v-model:user-name="bruker1" v-model:user-name2="bruker2"/>
   <MyClicker v-model:globalt-tall="tall" @klikki-paa="tall++"/>
</template>
