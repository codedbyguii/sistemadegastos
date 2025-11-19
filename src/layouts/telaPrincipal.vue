<template>

  <div class="navbar bg-base-100 shadow-sm">
  <div class="flex-1">
    <a class="btn btn-ghost text-xl">Controle de Gastos</a>
  </div>
  <div class="flex-none">
    <ul class="menu menu-horizontal px-1">
      <li>
        <details>
          <summary>Opções</summary>
          <ul class="bg-base-100 rounded-t-none p-2">
            <li><a href="/src/layouts/dashboard/dashboardSpending.vue">Gastos</a></li>
          </ul>
        </details>
      </li>
    </ul>
  </div>
</div>

  <h1 class="text-4xl text-center mt-20 font-bold">Controle de Gastos</h1>
  <p class="text-center mt-6">Um sistema simples para registrar e acompanhar suas despesas</p>

  <h2 class="font-bold ml-105 mt-15">Adicionar Despesa</h2>


  <div class="flex">
  <fieldset class="fieldset ml-105">
  <legend class="fieldset-legend">Descrição</legend>
  <input type="text" class="input rounded-none w-65" placeholder="Exemplo: Mercado" v-model="descricao"/>
  </fieldset>

  <fieldset class="fieldset ml-10 ">
  <legend class="fieldset-legend">Valor</legend>
  <input type="text" class="input rounded-none w-65" placeholder="R$" value="R$ " v-model="valor"/>
  </fieldset>
  </div>

  <button class="btn btn-outline btn-success ml-221 rounded-none mt-9">Adicionar</button>


  <div class="toast">
  <div class="alert alert-success">
    <span class="font-bold">Seu gasto foi atualizado!</span>
  </div>
</div>

</template>

<script></script>
