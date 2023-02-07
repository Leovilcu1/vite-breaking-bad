<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
export default{
  name:"App",
  components:{
    AppHeader,
    AppMain,
  },
 
   
}
</script> 

<template>
  <div class="bg-secondary">
    <AppHeader />
    <AppMain/>
  </div>
</template>

<style lang="scss">
@use '../styles/main.scss' as *;
</style>


