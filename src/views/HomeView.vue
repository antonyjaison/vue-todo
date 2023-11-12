<script>
import PopularSection from '../components/PopularSection.vue'
import BottomNav from '../components/BottomNav.vue'
export default {
    data() {
        return {
            artist: ""
        }
    },
    methods: {
        changeText: function () {
            this.$router.push("/artists")
        }
    },
    components: {
        PopularSection,
        BottomNav
    }

}
</script>



<template>
    <div class="home_wrapper">
        <h1>Hi There,<br><span>Anima</span></h1>
        <div class="input_wrapper">
            <i class="fa-solid fa-magnifying-glass"></i>
            <input v-on:change="changeText" @input="e => artist = e.target.value" :value="artist" type="text"
                placeholder="Search Artists">
        </div>

        <div class="your_playlist_card">
            <h1>Your Artists</h1>
            <div class="playlist_card">
                <div class="playlist_card_image">
                    <img src="../assets/images/playlist_1.jpg" alt="">
                </div>
                <div class="playlist_card_image">
                    <img src="../assets/images/playlist_1.jpg" alt="">
                </div>
                <div class="playlist_card_image">
                    <i class="fa-sharp fa-light fa-music-note"></i>
                </div>
                <div class="playlist_card_image">

                </div>
            </div>
            <div class="total_artists">
                <h2>Favorite Artists</h2>
                <p>2 Artists</p>
            </div>
        </div>
        <div class="popular_section">
            <h1>Popular</h1>
            <PopularSection />
        </div>

        <div class="popular_section">
            <h1>Popular</h1>
            <PopularSection />
        </div>

        <div class="popular_section">
            <h1>Popular</h1>
            <PopularSection />
        </div>
    </div>
    <BottomNav/>

</template>


<style scoped>
.home_wrapper {
    min-height: 100vh;
    width: 100%;
    background: linear-gradient(168.55deg, #212121 0%, #0B0B0B 100%);
    padding: 8% 5%;
    display: flex;
    flex-direction: column;
    gap: 20px;
    padding-bottom: 80px;
}

.home_wrapper>h1 {
    color: #23E5B5;
    font-size: 2.5rem;
    line-height: 40px;
}

.home_wrapper>h1>span {
    color: #fff;
    font-size: 1.5rem;
}

.home_wrapper .input_wrapper {
    width: 100%;
    height: 40px;
    border-radius: 5px;
    border: none;
    background-color: #212121;
    padding-left: 10px;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    gap: 15px;
}

.home_wrapper .input_wrapper i {
    color: #23E5B5;
}

.home_wrapper .input_wrapper input {
    background-color: transparent;
    border: none;
    color: #fff;
}

.home_wrapper .input_wrapper input::placeholder {
    color: #a7a7a7;
}

.home_wrapper input:focus {
    outline: none;
}

.your_playlist_card {
    width: 150px;
    display: flex;
    flex-direction: column;
    gap: 5px;
}

.your_playlist_card h1,
.trending_section h1,
.popular_section h1 {
    font-size: 1.1rem;
    color: #23E5B5;
}

.playlist_card {
    width: 150px;
    height: 150px;
    background-color: #272727;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    gap: 1px;
    border-radius: 5px;
}

.playlist_card_image {
    background-color: #212121;
}

.playlist_card_image:first-child {
    border-top-left-radius: inherit;
}

.playlist_card_image:nth-child(2) {
    border-top-right-radius: inherit;
}

.playlist_card_image:nth-child(3) {
    border-bottom-left-radius: inherit;
}

.playlist_card_image:last-child {
    border-bottom-right-radius: inherit;
}

.playlist_card_image img {
    width: 100%;
    height: 100%;
    border-radius: inherit;
    object-fit: cover;
}

.total_artists {
    text-align: center;
}

.total_artists {
    line-height: 13px;
}

.total_artists h2 {
    color: #fff;
    font-size: 0.7rem;
    font-weight: 400;
}

.total_artists p {
    color: #a7a7a7;
    font-weight: 400;
    font-size: 0.6rem;
}

.popular_section {
    display: flex;
    flex-direction: column;
    gap: 5px;
}
</style>