<template>
    <div id="list">
        <h3 class="text-uppercase">{{ pageTitle }} page <b class="text-danger">( {{ url }} )</b></h3>
        <div class="d-inline-flex flex-column fs-5">
            <div v-for="item in items" class="badge bg-info item mb-2">
                {{ pageTitle }} {{ item }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name : "Lists",
    props: ['items', 'pageTitle', 'url'],
    data() {
        return {

        }
    },
}
</script>

<style scoped>

</style>