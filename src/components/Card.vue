<template>
    <li class="text-center">
        <div class="ms-card">
            <div class="cover">
                <img :src="img" alt="title">
            </div>
            <div class="text">
                <h3>{{ title }}</h3>
                <h4>{{ subtitle }}</h4>
                <span>{{ year }}</span>
                <h6>{{ span }}</h6>
            </div>
        </div>
    </li>
</template>

<script>
export default {
    name: 'Card',
    props: {
        img: String,
        title: String,
        subtitle: String,
        year: String,
        span: String,
    }
}
</script>

<style scoped lang="scss">
@import '@/styles/colors.scss';

li {
    width: calc((100% / 8) - 35px);
    margin: 0 17.5px;
    padding: 20px;
    background-color: $bg_secondary;
    .text {
        h3,
        h6 {
            color: $color_primary;
        }
        h4,
        span {
            color: $color_secondary;
        }
    }
}

</style>