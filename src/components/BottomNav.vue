<template>
    <div class="bottom-navbar">
        <a href="#" class="nav-item">
            <i class="material-icons">home</i>
            <p>Home</p>
        </a>
        <a href="#" class="nav-item">
            <i class="material-icons">album</i>
            <p>My Albums</p>
        </a>
        <a href="#" class="nav-item">
            <i class="material-icons">person</i>
            <p>My Artists</p>
        </a>
        <a href="#" class="nav-item">
            <i class="material-icons">logout</i>
            <p>Logout</p>
        </a>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.bottom-navbar {
    position: fixed;
    bottom: 15px;
    left: 4%;
    right: 4%;
    background-color: #282828;
    display: flex;
    justify-content: space-around;
    padding: 8px 0;
    margin: 0 auto;
    max-width: calc(100% - 40px);
    /* Account for left and right margin */
    border-radius: 10px;
    box-shadow: rgba(255, 255, 255, 0.24) 0px 1px 8px;
}

.nav-item {
    text-decoration: none;
    color: #ffffff;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0;
}
.nav-item p {
    font-size: 10px;
    margin: 0;
}
</style>