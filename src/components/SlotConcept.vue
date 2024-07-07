<script lang="ts">
export default {}
</script>

<template>
  <div style="border: 1px solid black; margin: 5px">
    <p>Slot</p>
    <h2><slot name="titulo" /></h2>
    <p><slot name="corpo" /></p>
  </div>
</template>
