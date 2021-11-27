<template>
    <header class="p-1">
        <img src="../assets/logo (1).png" alt="Spotify Logo">
        <select @change="onChange">
            <option value="">All</option>
            <option v-for="(genre,index) in genres" :key="`genre ${index}`" :value="genre">
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
}
</style>