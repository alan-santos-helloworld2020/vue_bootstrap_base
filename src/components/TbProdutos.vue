<template>
  <div class="container">
    <b-table responsive striped hover :items="items" :fields="fields">
      <template class="d-flex flex-row" #cell(actions)="row">
        <b-button
          pill
          variant="primary"
          @click="editar(row.item)"
          class="rounded-circle"
        >
          <i class="material-icons p-1">edit</i>
        </b-button>

        <b-button
          pill
          variant="danger"
          @click="remover(row)"
          class="rounded-circle"
        >
          <i class="material-icons p-1">delete</i>
        </b-button>
      </template>
    </b-table>
  </div>
</template>

<script>
export default {
  name: "TbProdutos",
  data() {
    return {
      fields: [
        { key: "id", label: "Id" },
        { key: "nome", label: "Nome" },
        { key: "preco", label: "Preço" },
        { key: "cor", label: "Cor" },
        { key: "actions", label: "" },
      ],
      items: [
        { id: 1, nome: "geladeira", preco: "815,00", cor: "bege" },
        { id: 2, nome: "fogão", preco: "150.00", cor: "cinza" },
      ],
    };
  },
  methods: {
    editar(dados) {
      alert(dados.id);
    },
    remover(dados) {
      
      this.items.splice(dados.index, 1);
    },
  },
};
</script>

<style>
</style>