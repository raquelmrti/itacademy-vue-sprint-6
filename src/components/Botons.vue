<template>
  <button @click="$event => $emit('clickedBtn', 'back')">Anterior</button>
  <button @click="$event => $emit('clickedBtn', 'next')">Següent</button>
</template>

<script>
export default {
  name: "Botons",
  emits: ["clickedBtn"]
}

</script>

<style scoped>
button {
  flex-grow: 1;
  padding: 1em 0;
  font-size: 1.5em;
}
</style>