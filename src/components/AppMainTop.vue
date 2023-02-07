<script>
import {store} from '../store'
export default {
    name:"AppMainTop",
    data(){
        return{
            store
        }
    }
}
</script>

<template>
<footer >
    <div class="row justify-content-center mt-4 pt-4 ">
        <div class="col-11 bg-dark text-light p-2">
            Found {{store.characters.length}} characters
        </div>
    </div>
</footer>
</template>

<style lang="scss" scoped> 
</style>