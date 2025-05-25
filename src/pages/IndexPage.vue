<script setup>
import { ref } from 'vue'

const text1 = ref('Olá mundo!')

const alterarTexto = () => {
  if (text1.value === 'Olá mundo!') {
    text1.value = 'Texto alterado!'
  } else {
    text1.value = 'Olá mundo!'
  }
}
</script>

<template>
  <q-page class="flex flex-center column bg-dark">
    <h1 class="text-h2 text-white">{{ text1 }}</h1>

    <q-btn @click="alterarTexto" label="Mudar Texto" color="primary" class="q-mt-md" />
  </q-page>
</template>
