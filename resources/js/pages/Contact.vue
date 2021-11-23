<template>
    <div id="contact">
        <div class="container">
            <lists :page-title="pageTitle" :url="url" :items="items"></lists>
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
            url: this.$route.path,
            pageTitle: 'Contact',
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