<template>
    <main>
        <AlbumsComp/>
    </main>
</template>

<script>
import "bootstrap"
import AlbumsComp from '../components/AlbumsComp.vue'


export default {
    name: 'MainComp',
    components: {
    AlbumsComp
    }
}
</script>

<style scoped lang="scss">

@import "bootstrap/dist/css/bootstrap.min.css";

main {
    height: calc(100vh - 6vh);
    background-color: #1e2d3b;
    display: flex;
    justify-content: center;
    align-items: center;
}

</style>