<template>
  <button @click="$event => $emit('backOrForward', 'back')">Anterior</button>
  <button @click="$event => $emit('backOrForward', 'next')">Següent</button>
</template>

<script>
export default {
  name: 'Botons',
  emits: ['backOrForward']
}
</script>

<style scoped>
button {
  flex-grow: 1;
  padding: 1em 0;
  font-size: 1.5em;
}
</style>