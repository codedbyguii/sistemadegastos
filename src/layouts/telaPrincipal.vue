<template>

  <div class="navbar bg-base-200">
  <div class="ps-4">
    <a class="text-lg font-bold">Controle de Gastos</a>
  </div>
  <div class="flex grow justify-end px-2">
    <div class="flex items-stretch">
      <div class="dropdown dropdown-end">
        <div tabindex="0" role="button" class="btn btn-ghost rounded-field">=</div>
        <ul
          tabindex="-1"
          class="menu dropdown-content bg-base-200 rounded-box z-1 mt-4 w-52 p-2 shadow-sm">
          <li><a>Gastos</a></li>
        </ul>
      </div>
    </div>
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