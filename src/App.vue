<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
export default{
  name:"App",
  components:{
    AppHeader,
    AppMain,
  },
  data(){
    return{
      characters:[]
    }
  },
  created(){
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php' )
    .then((response) => {
      this.characters = response.data.data.slice(0,16);
    })
  }
}
</script>

<template>
  <div class="bg-secondary">
    <AppHeader />
    <AppMain :charactersList="characters"/>
  </div>
</template>

<style lang="scss">
@use '../styles/main.scss' as *;
</style>


