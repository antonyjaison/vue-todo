<template>
    <div class="artists_page">
        <div class="heading">
            <i :onClick="goBack" class="fa-solid fa-arrow-left"></i>
            <h3>Results for <span>Selena Gomez</span></h3>
        </div>
        <div class="artists_card_section">
            <ArtistCard name="Selena Gomez" imageUrl="" :addfavArtist="addfavArtist" />
        </div>
    </div>
</template>

<script>
import ArtistCard from '../components/ArtistCard.vue';
export default {
    components: {
        ArtistCard
    },
    methods: {
        goBack() {
            this.$router.push("/")
        },
        addfavArtist(name) {
            console.log(name)
        }
    }
}
</script>

<style scoped>
.artists_page {
    width: 100%;
    min-height: 100vh;
    background: linear-gradient(168.55deg, #212121 0%, #0B0B0B 100%);
    padding: 8% 5%;
}

.heading {
    display: flex;
    height: fit-content;
    align-items: center;
    gap: 20px;
}

.heading i {
    color: #fff;
    font-size: 20px;
    background-color: #272727;
    padding: 8px;
    border-radius: 50%;
    border: 1px solid #272727;
}

.heading h3 {
    color: #fff;
    font-size: 16px;
    margin-bottom: 25px;
    font-weight: 400;
    margin: 0;
}

.heading h3 span {
    font-weight: bold;
}

.artists_card_section {
    margin-top: 25px;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
}


</style>