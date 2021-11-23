<template>
    <div id="about">
        <div class="container">
            <!--            <lists :page-title="pageTitle" :url="url" :items="items"></lists>-->
            <div class="row mb-5 gap-3 ">
                <div @click="cardColor = btnColor" v-for="(btnColor,index) in btnColors" class="btn" :style="{backgroundColor: btnColor}" style="max-width: 8rem;">
                    {{ index }}
                </div>
            </div>
            <div class="row gap-3">
                <div class="card text-white mb-3" v-for="list in lists" :style="{backgroundColor: cardColor}" style="max-width: 18rem;">
                    <div class="card-header">Header</div>
                    <div class="card-body">
                        <h5 class="card-title">Primary card title</h5>
                        <p class="card-text">Some quick example text to build on the card title and make up the bulk of
                            the card's content.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Lists from "../components/Lists";

export default {
    name      : "About",
    components: {Lists},
    data() {
        return {
            url      : this.$route.path,
            pageTitle: 'About',
            items    : [
                'Item One',
                'Item Two',
                'Item Three',
                'Item Four',
            ],
            lists    : [1, 1, 1, 1, 1],
            cardColor: '#6cb2eb',
            btnColors : {
                blue:    '#0d6efd',
                indigo:  '#6610f2',
                purple:  '#6f42c1',
                pink:    '#d63384',
                red:     '#dc3545',
                orange:  '#fd7e14',
                yellow:  '#ffc107',
                green:   '#198754',
                teal:    '#20c997',
                cyan:    '#0dcaf0',
            },
        }
    }

}
</script>

<style scoped>

</style>