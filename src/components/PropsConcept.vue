<script lang="ts">
export default {
  props: {
    meuNome: {
      required: true,
      type: String
    }
  }
}
</script>

<template>
  <div>
    <p>Props</p>
    <p>{{ meuNome }}</p>
  </div>
</template>
