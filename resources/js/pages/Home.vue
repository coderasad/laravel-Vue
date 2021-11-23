<template>
    <div id="home">
        <div class="container">
            <lists :page-title="pageTitle" :url="url" :items="items"></lists>
            <button @click="showAlert" class="btn btn-danger">Hello world</button>
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
            url: this.$route.path,
            pageTitle: 'Home',
            items: [
                'Item One',
                'Item Two',
                'Item Three',
                'Item Four',
            ],
        }
    },
    mounted() {
        console.log(this.url)
    },

    methods: {
        showAlert() {
            const Toast = this.$swal.mixin({
                toast: true,
                position: 'top-end',
                showConfirmButton: false,
                timer: 3000,
                timerProgressBar: true,
                didOpen: (toast) => {
                    toast.addEventListener('mouseenter', this.$swal.stopTimer)
                    toast.addEventListener('mouseleave', this.$swal.resumeTimer)
                }
            })

            Toast.fire({
                icon: 'success',
                title: 'Signed in successfully'
            })

            // Use sweetalert2
           /* this.$swal.fire({
                position: 'top-end',
                icon: 'success',
                title: 'Your work has been saved',
                showConfirmButton: false,
                toast : true,
                timerProgressBar : true,
                timer: 2500
            })*/
        },
    }

}
</script>

<style scoped>

</style>