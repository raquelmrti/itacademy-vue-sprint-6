<template>
  <p v-for='(frase, i) in frases' :key='i' :class='{ active: i === currentSentence }'>
    {{ frase.txt }}
  </p>
</template>

<script>
export default {
  name: 'Escena',
  props: {
    frases: Array,
    currentSentence: Number
  },
}
</script>

<style scoped>
p {
  background-color: #ffffffbe;
  padding: .7em;
  border: 2px solid black;
  border-radius: 20px;
  text-align: center;
}

.active {
  background-color: #ffb7b7;
}
</style>
