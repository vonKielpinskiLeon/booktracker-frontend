<script setup lang="ts">
interface Buch {
  titel: string
  autor: string
  bewertung: number
}

defineProps<{
  buecher: Buch[]
}>()
</script>

<template>
  <div>
    <h2>Meine Bücher</h2>
    <ul>
      <li v-for="buch in buecher" :key="buch.titel">
        {{ buch.titel }} von {{ buch.autor}} ({{ buch.bewertung }}/5 Sternen)
      </li>
    </ul>
  </div>
</template>

<style scoped></style>
