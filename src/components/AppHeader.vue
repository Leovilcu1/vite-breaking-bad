<script>

import imputForm from './imputForm.vue';

export default {
    name:"AppHeader",
    components:{
        imputForm
    }
}
</script>

<template>
<header>
    <div>LOGO</div>
    <div class="container">
        <imputForm/>
    </div>
</header>
</template>

<style lang="scss" scoped>
</style>