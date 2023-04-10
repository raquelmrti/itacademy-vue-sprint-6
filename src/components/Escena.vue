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
