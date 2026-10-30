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
        {{ buch.titel }} von {{ buch.autor }} ({{ buch.bewertung }}/5 Sternen)
      </li>
    </ul>
  </div>
</template>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}

li {
  padding: 15px;
  margin-bottom: 15px;
  background-color: #223;
}
</style>
