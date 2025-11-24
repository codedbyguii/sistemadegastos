<template>
  <div class="container">
    <h1 class="text-center font-bold text-6xl mt-25">Controle de Gastos</h1>

    <FormGasto @add-gasto="adicionarGasto" />

    <ListaGastos :gastos="gastos" @excluirGasto="excluirGasto" />

    <h2 class="text-center font-bold text-xl mt-9">Total: R$ {{ total }}</h2>
  </div>
</template>

<script>
import FormGasto from '../components/FormGasto.vue'
import ListaGastos from '../components/ListaGastos.vue'

export default {
  components: { FormGasto, ListaGastos },

  data() {
    return {
      gastos: []
    }
  },

  computed: {
    total() {
      return this.gastos.reduce((acc, g) => acc + g.valor, 0)
    }
  },

  methods: {
    adicionarGasto(gasto) {
      this.gastos.push(gasto)
    },
    excluirGasto(index) {
      this.gastos.splice(index, 1)
    }
  }
}
</script>

<style>
.container {
  max-width: 600px;
  margin: auto;
  padding: 20px;
}
</style>
