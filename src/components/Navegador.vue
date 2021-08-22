<template>
  <b-navbar class="p-2" toggleable="mb" type="dark" variant="danger">
    <b-navbar-brand :to="{name:'Home'}">Onload</b-navbar-brand>

    <b-navbar-toggle target="navbar-toggle-collapse">
      <template #default="{ expanded }">
        <b-icon v-if="expanded" icon="chevron-bar-up"></b-icon>
        <b-icon v-else icon="chevron-bar-down"></b-icon>
      </template>
    </b-navbar-toggle>

    <b-collapse id="navbar-toggle-collapse" is-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-item :to="{name:'Home'}">Home</b-nav-item>
        <b-nav-item :to="{name:'Cadastro'}">Cadastro</b-nav-item>
        <b-nav-item :to="{name:'Tabela'}">Tabela</b-nav-item>
        <b-nav-item :to="{name:'Sobre'}">Sobre</b-nav-item>
        <!-- <b-nav-item href="#" disabled>Disabled</b-nav-item> -->
      </b-navbar-nav>
    </b-collapse>

  </b-navbar>
</template>

<script>
export default {
  name: "Navegador",
  props: {
    msg: String,
  },
};
</script>


<style scoped>
</style>
