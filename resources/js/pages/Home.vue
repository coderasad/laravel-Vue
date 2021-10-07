<template>
    <div id="home">
        <div class="container">
            <h3 class="text-uppercase">home page {{ parentValue }}</h3>
            <lists :name="name" :items="items"></lists>
        </div>
    </div>
</template>

<script>
import Lists from "../components/Lists";
export default {
    name: "Home",
    components: {Lists},
    data(){
        return{
            name: 'Home',
            items: [
                'Item One',
                'Item Two',
                'Item Three',
                'Item Four',
            ],
            parentValue:'',
        }
    },

}
</script>

<style scoped>

</style>