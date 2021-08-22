<template>
  <div class="b-container">
      <Navegador></Navegador>
      <div class="row">
          <div class="col-lg-12 text-center">
              <p class="mt-5">Tabela de Produtos</p>
              <TbProdutos></TbProdutos>

          </div>
      </div>
  </div>
</template>

<script>
import Navegador from "../components/Navegador.vue";
import TbProdutos from "../components/TbProdutos.vue";
export default {


    components:{
        Navegador,
        TbProdutos
    }

}
</script>

<style>

</style>