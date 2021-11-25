<template>
    <section class="list ms-container d-flex justify-content-center align-items-center h-100">
        <ul class="row col-12 justify-content-center flex-wrap">
            <li class="text-center">
                <div class="ms-card">
                    <div class="cover">
                        <img src="../assets/logo (1).png" alt="">
                    </div>
                    <div class="text">
                        <h3>Title</h3>
                        <h4>Subtitle</h4>
                        <span>span</span>
                        <h6>span</h6>
                    </div>
                </div>
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    name: 'CardList',
}
</script>

<style scoped lang="scss">
@import '@/styles/colors.scss';

.list {
    &.ms-container {
        max-width: 1920px;
        margin: 0 80px;
    }
    color: #fff;
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
}

</style>