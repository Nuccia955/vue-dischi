<template>
    <header class="p-1">
        <img src="../assets/logo (1).png" alt="Spotify Logo">
        <select @change="onChange">
            <option value="">All</option>
            <option value="Metal">Metal</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
        </select>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            optionActive: '',
        }
    },
    methods: {
        onChange(event) {
            this.$emit('selectGenre', event.target.value);
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