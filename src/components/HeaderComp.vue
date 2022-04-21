<template>
    <header class="bg_grey_custom">
        <img class="m-2" src="../assets/spotify-logo.png" alt="Spotify logo">
    </header>
</template>

<script>
import "bootstrap"

export default {
    name: 'HeaderComp',
    components: {
    // HelloWorld
    }
}
</script>

<style scoped lang="scss">

@import "bootstrap/dist/css/bootstrap.min.css";

header {
    height: 6vh;
    display: flex;
}

.bg_grey_custom {
    background-color: #2e3a46;
}

</style>