<script>
import{store} from '../store';
import axios from 'axios';
import imputForm from './imputForm.vue';

export default {
    name:"AppHeader",
    components:{
        imputForm
    },
    data(){
        return{
        store
        }
    },
    methods:{
        getCharacters(){
            axios
            .get('https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=' + this.store.categoriValue )
            .then((response) => {
                this.store.characters = response.data.data.slice(0,16);
            })
        }
    },
    created (){
        axios
            .get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
            .then((response) => {
                this.store.characters = response.data.data.slice(0,90);
            })
    }
    
}
</script>

<template>
    
<header>
    <div>LOGO</div>
    <div class="container">
        <imputForm @search ="getCharacters"/>
    </div>
</header>
</template>

<style lang="scss" scoped>
</style>