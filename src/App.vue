<script lang="ts">
import PropsConcept from './components/PropsConcept.vue'
import EmitConcept from './components/EmitConcept.vue'
import WatcherConcept from './components/WatcherConcept.vue'
import SlotConcept from './components/SlotConcept.vue'
import FormConcept from './components/FormConcept.vue'

export default {
  components: {
    PropsConcept,
    EmitConcept,
    WatcherConcept,
    SlotConcept,
    FormConcept
  },
  data() {
    return {
      mensagem: 'Olá mundo!',
      nomeUsuario: 'Pietro',
      lista: [{ name: 'pietro' }, { name: 'carol' }, { name: 'cesar' }],
      forca: 5,
      vitalidade: 7,
      meuNome: 'Pietro',
      alerta: ''
    }
  },
  methods: {
    consoleLog() {
      console.log('Olá mundo!')
    },
    receberAlerta(alerta: string) {
      this.alerta = alerta
    }
  },
  computed: {
    hpPersonagem() {
      return this.forca * this.vitalidade
    }
  }
}
</script>

<template>
  <div>
    <p>renderização variavel</p>
    <p>{{ mensagem }}</p>
  </div>
  <hr />
  <p>método</p>
  <button @click="consoleLog">Console log!</button>
  <hr />
  <p>renderização condicional</p>
  <p v-if="nomeUsuario.length > 0">{{ nomeUsuario }}</p>
  <p v-else>Nome não existe!</p>
  <hr />
  <p>Listagem</p>
  <ul v-for="(item, index) in lista" :key="`item.name-${index}`">
    <li>{{ item.name }}</li>
  </ul>
  <hr />
  <p>Variavel computada</p>
  <p>{{ hpPersonagem }}</p>
  <hr />
  <PropsConcept :meu-nome="meuNome" />
  <hr />
  <EmitConcept @alerta="receberAlerta" />
  <p>{{ alerta }}</p>
  <hr />
  <WatcherConcept />
  <hr />
  <SlotConcept>
    <template v-slot:titulo>Eu sou o titulo!</template>
    <template v-slot:corpo>Eu sou o corpo!</template>
  </SlotConcept>
  <hr />
  <FormConcept />
  <hr />
</template>

<style scoped></style>
