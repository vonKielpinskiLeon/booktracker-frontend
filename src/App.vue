<script setup lang="ts">
import { onMounted, ref } from 'vue'
import BuchListe from './components/BuchListe.vue'

const buecher = ref([])


onMounted(async () => {
  const baseURL = import.meta.env.VITE_BACKEND_BASE_URL

  try{
    const response = await fetch(baseURL + '/')
    buecher.value = await response.json()
  } catch (error){
    console.error('Fehler beim Laden der Bücher: ', error)
  }
})
</script>

<template>
  <main>
    <h1>Booktracker</h1>
    <BuchListe :buecher="buecher" />
  </main>
</template>

<style scoped></style>
