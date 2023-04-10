<template>
  <p v-for="frase in frases">
    {{ frase }}
  </p>
</template>

<script>
export default {
  props: ["frases"]
}
</script>

<style scoped>
p {
  border: 2px solid black;
  border-radius: 20px;
  padding: .5em;
  text-align: center
}
</style>
