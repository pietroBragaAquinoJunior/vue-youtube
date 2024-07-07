<script lang="ts">
export default {
  data() {
    return {
      nome: ''
    }
  },
  methods: {
    enviarFormulario() {
      console.log(this.nome)
    }
  }
}
</script>

<template>
  <div>
    <p>Formulario</p>
    <div>
      <label for="inputNome">Digite seu nome </label>
      <input id="inputNome" v-model="nome" />
      <p>Valor do input: {{ nome }}</p>
      <button @click="enviarFormulario">Enviar formulario!</button>
    </div>
  </div>
</template>
