<template>
  <div class="b-container">
    <Navegador></Navegador>
    <div class="row">
      <div class="col-10 offset-1 col-lg-8 offset-lg-2 mt-5">
          <p class="text-center"><b>Formulário de cadastro de produtos</b></p>
        <b-form @submit.prevent="enviar">
          <b-form-group
            id="input-group-1"
            label="Nome do Produto:"
            label-for="input-1"
            class="mt-3"
          >
            <b-form-input
              id="input-1"
              v-model="dados.nome"
              type="text"
              placeholder=""
              required
            ></b-form-input>
          </b-form-group>

          <b-form-group
            id="input-group-2"
            label="Descrição do Produto:"
            label-for="input-2"
            class="mt-3"
          >
            <b-form-input
              id="input-2"
              v-model="dados.descricao"
              type="text"
              placeholder=""
              required
            ></b-form-input>
          </b-form-group>

          <b-form-group
            id="input-group-3"
            label="Cor do Produto:"
            label-for="input-3"
            class="mt-3"
            content-cols-lg="6"
          >
            <b-form-input
              id="input-3"
              v-model="dados.cor"
              type="text"
              placeholder=""
              required
            ></b-form-input>
          </b-form-group>

          <b-form-group
            id="input-group-4"
            label="Preço do Produto:"
            label-for="input-4"
            class="mt-3"
            content-cols-lg="6"
          >
            <b-input
              id="input-4"
              v-model="dados.preco"
              type="text"
              v-mask="money"
              placeholder="R$ 000.000,00"
              required
            ></b-input>
          </b-form-group>

    
        <b-button class="mt-3" size="lg" type="submit" variant="primary">
            <b-icon icon="gear-fill" aria-hidden="true"></b-icon> Cadastrar
        </b-button>
        
        </b-form>
      </div>
    </div>
  </div>
</template>

<script>
import Navegador from "../components/Navegador.vue";
import createNumberMask from 'text-mask-addons/dist/createNumberMask';
  const currencyMask = createNumberMask({
    suffix:"",
    prefix: 'R$ ',
    allowDecimal: true,
    thousandsSeparatorSymbol:".",
    decimalSymbol:",",
    decimalLimit:2,
    includeThousandsSeparator: true,
    allowNegative: false,
  });
export default {
  data() {
    return {
      dados: {
        nome: null,
        descricao: null,
        cor: null,
        preco: null,
      },
      money:currencyMask
      
    }
  },
  methods:{
      enviar(){
          alert(JSON.stringify(this.dados))
      }

  },
  components: {
    Navegador,
  },
};
</script>