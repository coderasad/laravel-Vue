<template>
    <div id="list">
        <div class="d-inline-flex flex-column fs-5">
            <div v-for="item in items"  class="badge bg-info item mb-2">
               {{ name }} {{ item }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Lists",
    props: ['name', 'items'],
    data() {
        return{
            parentValue: 'testValue'
        }
    },
    mounted() {
        this.$parent.parentValue = this.parentValue;
    }
}
</script>

<style scoped>

</style>