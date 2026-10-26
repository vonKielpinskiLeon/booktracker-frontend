<script setup lang="ts">
import { ref } from 'vue'
import BuchListe from './components/BuchListe.vue'

const buecher = ref([
  { titel: 'Der Herr der Ringe', autor: 'J.R.R. Tolkien', bewertung: 5 },
  { titel: 'Harry Potter', autor: 'J.K. Rowling', bewertung: 4}
])
</script>

<template>
  <main>
    <h1>Booktracker</h1>
    <BuchListe :buecher="buecher" />
  </main>
</template>

<style scoped>
</style>
