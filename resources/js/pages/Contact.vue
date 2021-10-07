<template>
    <div id="contact">
        <div class="container">
            <h3 class="text-uppercase">
                contact page
            </h3>
            <lists :name="name" :items="items"></lists>
        </div>
    </div>
</template>

<script>
import Lists from "../components/Lists";
export default {
    name: "Contact",
    components: {Lists},
    data(){
        return{
            name: 'Contact',
            items: [
                'Item One',
                'Item Two',
                'Item Three',
                'Item Four',
            ],
        }
    }
}
</script>

<style scoped>

</style>