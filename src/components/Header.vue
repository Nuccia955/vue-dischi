<template>
    <header class="p-1">
        <img src="../assets/logo (1).png" alt="Spotify Logo">
        <select @change="onChange">
            <option value="">All</option>
            <option v-for="(genre,index) in filterGenres" :key="`genre ${index}`" :value="genre">
                {{ genre }}
            </option>
            <!-- <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option> -->
        </select>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            genres: [],
        }
    },
    props: {
        list: Array,
    },
    computed: {
        filterGenres() {
            this.getGenres();
            return this.genres;
        }
    },
    methods: {
        onChange(event) {
            this.$emit('selectGenre', event.target.value);
        },
        getGenres() {
            this.list.forEach(album => {
                if(!this.genres.includes(album.genre)) {
                    this.genres.push(album.genre)
                }
            })
        }
    }
}
</script>

<style scoped lang="scss">
@import '@/styles/colors.scss';
header {
    background-color: $bg_secondary;
    img {
        width: 40px;
    }
}
</style>