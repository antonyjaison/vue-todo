<template>
    <div class="card-container">
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
    </div>
</template>

<script>
import Card from './Card.vue';
export default  {
    components: {
        Card
    }
}
</script>

<style scoped>
.card-container {
    width: 100%;
    overflow-x: scroll;
    white-space: nowrap;
}

.card-container::-webkit-scrollbar {
    display: none;
}
</style>