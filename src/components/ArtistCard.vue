        
<script>
export default {
    props: {
        imageUrl: {
            type: String,
            required: true
        },
        name: {
            type: String,
            required: true,
        },
        addfavArtist: {
            type: Function,
            required: true
        }
    },
}
</script>

<template>
    <div class="artist_card">
        <img src="../assets/artist.png" alt="">
        <p>{{ name }}</p>
        <i @click="() => addfavArtist(name)" class="material-icons-outlined">favorite</i>
    </div>
</template>

<style scoped>
.artist_card {
    position: relative;
    width: 100px;
    height: fit-content;
}

.artist_card img {
    width: 100px;
    height: 100px;
    object-fit: cover;
}

.artist_card p {
    color: #fff;
    font-style: normal;
    font-weight: 500;
    font-size: 12px;
    line-height: 20px;
    text-align: center;
}

.artist_card i {
    position: absolute;
    bottom: 22%;
    right: 0;
    font-size: 40px;
    color: #fff;
}
</style>