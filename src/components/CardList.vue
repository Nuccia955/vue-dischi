<template>
    <section class="list ms-container d-flex justify-content-center align-items-center h-100">
        <ul class="row col-12 justify-content-center flex-wrap">
            <Card v-for="(album, index) in albums" :key="`album ${index}`"
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
import axios from 'axios'
import Card from '@/components/Card.vue'
export default {
    name: 'CardList',
    data() {
        return {
            albums: null,
        }
    },
    components: {
        Card,
    },
    created() {
        this.getAlbums();
    },
    methods: {
        getAlbums() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music').then(result => {
                this.albums = result.data.response;
                console.table(this.albums);
            }).catch(error => console.log(error));
        }
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