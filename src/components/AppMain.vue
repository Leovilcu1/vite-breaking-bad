<script>
import {store} from '../store'
import AppMainTop from './AppMainTop.vue';
export default {
    name:"AppMain",
  
    data(){
        return{
            store,
        }
    },
    components:{
        AppMainTop
    },
} 
</script>

<template>
    <main>
    <div class="container bg-light">
        <AppMainTop/>
        <div class="row justify-content-center py-3">
            <div class="col-11">
                <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 row-cols-lg-4 g-4">
                    <div class="col text-center bg-secondary p-2  " v-for="character in store.characters">
                        <div v-for="i in character.card_images.slice(0,15)">
                            <img :src="i.image_url_small" alt="character.name">                       
                        </div>
                        <h3>{{ character.name}}</h3>
                        <h5>{{character.archetype}}</h5>
                    </div>
                </div>
            </div>
        </div>
    </div>
    </main>
</template> 

<style lang="scss" scoped>
</style>