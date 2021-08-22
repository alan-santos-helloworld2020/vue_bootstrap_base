<template>
  <div class="row">
    <router-view></router-view>
  </div>
</template>

<script>

import router from './router/index.js'

export default({
  data() {
    return{


    }
    
  },
  created(){
    router.push({name:'Home'})

  },
  components:{
   
  }
})
</script>

<style>

</style>
