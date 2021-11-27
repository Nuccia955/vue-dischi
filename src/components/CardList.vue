<template>
    <section class="list ms-container d-flex justify-content-center align-items-center h-100">
        <ul class="row col-12 justify-content-center flex-wrap">
            <Card v-for="(album, index) in list" :key="`album ${index}`"
                :img="album.poster" 
                :title="album.title" 
                :subtitle="album.author" 
                :year="album.year" 
                :span="album.genre"
            />
        </ul>
    </section>
</template>

<script>
import Card from '@/components/Card.vue'
export default {
    name: 'CardList',
    components: {
        Card,
    },
    props: {
        list: Array,
    }

}
</script>

<style scoped lang="scss">
.list {
    &.ms-container {
        max-width: 1920px;
        margin: 0 80px;
    }
}
</style>