<script lang="ts">
export default {
  emits: ['alerta']
}
</script>

<template>
  <div>
    <p>Emit</p>
    <button @click="$emit('alerta', 'Alerta vermelho!')">Emitir Alerta!</button>
  </div>
</template>
