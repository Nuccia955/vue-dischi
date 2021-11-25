<template>
    <section class="list ms-container d-flex justify-content-center align-items-center h-100">
        <ul class="row col-12 justify-content-center flex-wrap">
            <li>
                <div class="ms-card">
                    <h1>album</h1>
                </div>
            </li>
            <li>
                <div class="ms-card">
                    <h1>album</h1>
                </div>
            </li>
            <li>
                <div class="ms-card">
                    <h1>album</h1>
                </div>
            </li>
            <li>
                <div class="ms-card">
                    <h1>album</h1>
                </div>
            </li>
            <li>
                <div class="ms-card">
                    <h1>album</h1>
                </div>
            </li>
            <li>
                <div class="ms-card">
                    <h1>album</h1>
                </div>
            </li>
            <li>
                <div class="ms-card">
                    <h1>album</h1>
                </div>
            </li>
            <li>
                <div class="ms-card">
                    <h1>album</h1>
                </div>
            </li>
            <li>
                <div class="ms-card">
                    <h1>album</h1>
                </div>
            </li>
            <li>
                <div class="ms-card">
                    <h1>album</h1>
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
    }
}

</style>