<script>
import{store} from '../store'
   export default {
    name:"imputForm",
    data(){
        return{
            store
        }
    },
   };


</script>

<template>

    <form action="">
        <div class="row">
            <div class="col-auto">
                <select v-model="store.categoriValue" @change="$emit('search')" id="formSelect" aria-label="select status">
                    <option selected value="">Select Categori</option>
                    <option value="alien">Alien</option>
                    <option value="noble knight">Noble Knight</option>
                    <option value="melodius">Melodious</option>
                </select>
            </div>
        </div>
    </form>
  
</template>

<style lang="scss" scoped>
</style>