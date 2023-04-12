<template>
  <p v-for="(frase, i) in frases" :key="i" :class="{ active: i === currentSentence }">
    {{ frase }}
  </p>
</template>

<script>
export default {
  name: "Escena",
  props: {
    frases: Array,
    currentSentence: Number
  },
}
</script>

<style scoped>
p {
  border: 2px solid black;
  border-radius: 20px;
  padding: .5em;
  text-align: center
}

.active {
  background-color: #ff9d9d;
}
</style>
