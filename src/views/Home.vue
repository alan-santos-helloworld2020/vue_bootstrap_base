<template>
  <b-container>
    <Navegador></Navegador>
    <div class="row">
      <div class="col-lg-12 text-center">
        <p class="mt-5">Home</p>
      </div>
    </div>
  </b-container>
</template>

<script>
// @ is an alias to /src
import Navegador from '@/components/Navegador.vue'

export default {
  name: 'Home',
  components: {
    Navegador
  }
}
</script>
