<script lang="ts">
export default {
  data() {
    return {
      meObserve: 'Me observe'
    }
  },
  methods: {
    mudarValorVariavel() {
      this.meObserve = 'Eu mudei! (observe o log do watcher)'
    }
  },
  watch: {
    meObserve(novoValor, velhoValor) {
      console.log(velhoValor + ' - ' + novoValor)
    }
  }
}
</script>

<template>
  <div>
    <p>Watcher</p>
    <p>{{ meObserve }}</p>
    <button @click="mudarValorVariavel">Mudar o valor</button>
  </div>
</template>
