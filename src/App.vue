<script setup>
import { ref } from 'vue';
import CryptoForm from './components/CryptoForm.vue';

const submittedText = ref('');

function handleTextSubmitted(text) {
  submittedText.value = text;
}
</script>

<template>
  <CryptoForm @text-submitted="handleTextSubmitted" />
  <div v-if="submittedText">
    <h2>Submitted Text:</h2>
    <pre>{{ submittedText }}</pre>
  </div>
</template>
