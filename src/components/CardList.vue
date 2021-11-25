<template>
    <section class="list ms-container d-flex justify-content-center align-items-center h-100">
        <ul class="row col-12 justify-content-center flex-wrap">
            <Card 
                :img="require(`../assets/logo (1).png`)" 
                title="title" 
                subtitle="subtitle" 
                year="year" 
                span="span"
            />
        </ul>
    </section>
</template>

<script>
import Card from '@/components/Card.vue'
export default {
    name: 'CardList',
    components: {
        Card,
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