<template>
  <form @submit.prevent="enviar">
    <div class="flex mt-15">
    <input class="input rounded-none" v-model="descricao" placeholder="Exemplo: Mercado" />
    <input class="input ml-9 rounded-none" v-model.number="valor" type="number" placeholder="Exemplo: R$ 100" />
    </div>
    <button class="btn ml-116 rounded-none btn-primary mt-3">Adicionar</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      descricao: "",
      valor: null
    }
  },

  methods: {
    enviar() {
      if (!this.descricao || !this.valor) return

      this.$emit("add-gasto", {
        descricao: this.descricao,
        valor: this.valor
      })

      this.descricao = ""
      this.valor = null
    }
  }
}
</script>
