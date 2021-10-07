<template>
    <div id="about">
        <div class="container">
            <h3 class="text-uppercase">
                About Page
            </h3>
            <lists :name="name" :items="items"></lists>
        </div>
    </div>
</template>

<script>
import Lists from "../components/Lists";
export default {
    name: "About",
    components: {Lists},
    data(){
        return{
            name: 'About',
            items: [
                'Item One',
                'Item Two',
                'Item Three',
                'Item Four',
            ]
        }
    }
}
</script>

<style scoped>

</style>