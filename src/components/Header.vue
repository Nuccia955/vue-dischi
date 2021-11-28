<template>
    <header class="p-1 d-flex align-items-center justify-content-between">
        <img src="../assets/logo (1).png" alt="Spotify Logo">
        <select class="mx-4" @change="onChange">
            <option class="custom-option" value="">All</option>
            <option class="custom-option" v-for="(genre,index) in genres" :key="`genre ${index}`" :value="genre">
                {{ genre }}
            </option>
        </select>
    </header>
</template>

<script>
export default {
    name: 'Header',
    props: {
        genres: Array,
    },
    methods: {
        onChange(event) {
            this.$emit('selectGenre', event.target.value);
        },
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
    select, 
    select option.custom-option {
        width: 100px;
        background-color: $bg_primary;
        padding: 5px 10px;
        border-color: transparent;
        border-radius: 5px;
        color: $color_theme;
    }
}
</style>