<template>
  <div v-if='!wasStartButtonClicked'>
    <h1>Benvingut!</h1>

    <p>Aquest és un prototip per a una aplicació destinada a mostrar consells relacionats amb la gestió empresarial. Com
      que encara està en fase de prova i no disposem del material real que s'utilitzarà, es mostraràn frases
      d'un petit relat.
    </p>

    <p>Amb els botons d'anterior i següent es pot passar d'una frase a l'altra.</p>

    <button @click='start'>Començar</button>
  </div>

  <div v-else class='container' :style='backgroundImg'>
    <div class='buttons'>
      <Botons @backOrForward='navigateThroughPhrases' />
    </div>

    <Escena :frases='frases' :currentSentence='currentSentence' />
  </div>
</template>

<script>
import Botons from './Botons.vue'
import Escena from './Escena.vue'
import frases from '../assets/frases'

export default {
  name: 'Home',
  components: {
    Botons,
    Escena
  },
  data() {
    return {
      frases: frases,
      currentSentence: 0,
      wasStartButtonClicked: false,
    }
  },
  methods: {
    start() {
      this.wasStartButtonClicked = true
    },
    navigateThroughPhrases(backOrForward) {
      if (backOrForward === 'back' && this.currentSentence > 0) {
        this.currentSentence--
      } else if (backOrForward === 'next' && this.currentSentence < this.frasesLength) {
        this.currentSentence++
      }
    }
  },
  computed: {
    frasesLength() {
      return this.frases.length - 1
    },
    backgroundImg() {
      return { backgroundImage: `url(img/${this.frases[this.currentSentence].img})` }
    }
  }
}
</script>

<style scoped>
div {
  padding: 1em;
}

.buttons {
  display: flex;
  flex-grow: 1
}

.container {
  background-size: cover;
  height: 100vh;
  padding: 1em
}
</style>