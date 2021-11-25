<template>
    <li class="text-center">
        <div class="ms-card">
            <div class="cover">
                <img :src="img" alt="title">
            </div>
            <div class="text">
                <h5 class="title">{{ title }}</h5>
                <h6 class="subtitle">{{ subtitle }}</h6>
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
    margin: 0 17.5px 20px;
    padding: 20px;
    background-color: $bg_secondary;
    .cover {
        margin-bottom: 1em;
        min-height: 95px;
        max-height: 150px;
    }
    .text {
        .title{
            font-size: 0.9em;
            line-height: 1.3em;
            margin-bottom: 15px;
            text-transform: uppercase;
            font-weight: 600;
        }
        .subtitle {
            font-size: 0.85em;
            margin: 0;
        }
        span {
            font-size: 0.8em;
        }
        h6 {
            margin: 0;
            font-size: 0.8em;
        }
        h5,
        h6 {
            color: $color_primary;
        }
        h6.subtitle,
        span {
            color: $color_secondary;
        }
    }
}

</style>