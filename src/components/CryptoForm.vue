<script setup>
import { ref } from 'vue';

const inputText = ref('');
const emit = defineEmits(['submit']);

function handleSubmit() {
    emit('submit', inputText.value);
}
</script>

<template>
    <form @submit.prevent="handleSubmit">
        <textarea v-model="inputText" id="crypto-input" rows="10" cols="50" placeholder="Type your plaintext or ciphertext here..."></textarea>
        <br />
        <button type="submit">Submit</button>
    </form>
</template>