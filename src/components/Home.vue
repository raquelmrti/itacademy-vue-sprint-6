<template>
  <Escena :frases="frases" />
</template>

<script>
import Escena from "./Escena.vue"
import frases from "../assets/frases.json"

export default {
  components: {
    Escena
  },
  data() {
    return {
      frases: frases
    }
  },
}
</script>