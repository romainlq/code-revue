<template>
    <div class="container">
        <Row v-for="row in list" v-bind:reviewer="row.reviewer" v-bind:reviewed="row.reviewed" :key="row.id"/>
    </div>
</template>

<script>
import Row from './Row'
export default {
    name: 'Table',
    components: {
        Row
    },
    props: {
        list: Array
    }
}
</script>

<style scoped>
.container {
    display: flex;
    flex-flow: column nowrap;
    justify-content: center;
    align-items: center;
}

</style>
