<template>
  <div>
    <Botons @clickedBtn="goBackOrForward" />
  </div>
  <Escena :frases="frases" :currentSentence="currentSentence" />
</template>

<script>
import Botons from "./Botons.vue"
import Escena from "./Escena.vue"

import frases from "../assets/frases.json"

export default {
  name: "Home",
  components: {
    Botons,
    Escena
  },
  data() {
    return {
      frases: frases,
      currentSentence: 0,
    }
  },
  methods: {
    goBackOrForward(clickedBtn) {
      if (clickedBtn === "back" && this.currentSentence > 0) {
        this.currentSentence--
      } else if (clickedBtn === "next" && this.currentSentence < this.frasesLength) {
        this.currentSentence++
      }
    }
  },
  computed: {
    frasesLength() {
      return this.frases.length - 1
    }
  }
}
</script>

<style scoped>
div {
  display: flex;
  flex-grow: 1
}
</style>