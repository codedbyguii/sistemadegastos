<template>
  <ul>
    <li class="text-center mt-9 font-bold ml-15" v-for="(gasto, index) in gastos" :key="index">
      {{ gasto.descricao }} ————— R$ {{ gasto.valor }}  <button
        class="btn btn-neutral rounded-none btn-sm ml-10"
        @click="$emit('excluirGasto', index)"
      >
        Excluir
      </button>
    </li>
  </ul>
</template>
<script>
export default {
  props: ["gastos"]
}
</script>
