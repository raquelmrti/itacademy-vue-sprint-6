<template>
  <div v-if="!wasStartButtonClicked">
    <h1>Benvingut!</h1>
    <p>Aquest és un prototip per a una aplicació destinada a mostrar consells relacionats amb la gestió empresarial. Com
      que encara està en fase de prova i no disposem del material real que s'utilitzarà, es mostraràn frases
      d'un conte.
    </p>
    <p>Amb els botons d'anterior i següent es pot passar d'una frase a l'altra.</p>
    <button @click="start">Començar</button>
  </div>

  <div v-if="wasStartButtonClicked">
    <div class="buttons">
      <Botons @clickedBtn="goBackOrForward" />
    </div>
    <Escena :frases="frases" :currentSentence="currentSentence" />
  </div>
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
      wasStartButtonClicked: false
    }
  },
  methods: {
    start() {
      this.wasStartButtonClicked = true
    },
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
.buttons {
  display: flex;
  flex-grow: 1
}
</style>