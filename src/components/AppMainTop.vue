<script>
export default {
    name:"AppMainTop",
    props:{
        totalCards:{
            type: Number,
            default: 0,
        }
    }
}
</script>

<template>
<footer >
    <div class="row justify-content-center mt-4 pt-4 ">
        <div class="col-11 bg-dark text-light p-2">
            Found {{totalCards}} characters
        </div>
    </div>
</footer>
</template>

<style lang="scss" scoped>
</style>