<template>
    <header class="p-1">
        <img src="../assets/logo (1).png" alt="Spotify Logo">
    </header>
</template>

<script>
export default {
    name: 'Header',
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