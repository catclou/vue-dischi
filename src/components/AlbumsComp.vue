<template>
    <!-- <div class="container"> -->
        <div class="row-cols-6 d-flex flex-wrap align-center riga_cust">
            <CardAlbum
                v-for="( element, index ) in albumsArray"
                :key="index"
                :poster="element.poster"
                :title="element.title"
                :author="element.author"
                :year="element.year"
            />

        <!-- </div> -->
    </div>
</template>

<script>
import "bootstrap"
import axios from 'axios';
import CardAlbum from './CardAlbum.vue'


export default {
    name: 'AlbumsComp',
    data(){
        return{
            albumsArray: []
        }
    },
    created(){

        // Chiamata ad Axios
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then( ( response )=>{
            console.log(response)
            this.albumsArray = response.data.response
        } )

    },
    components: {
    CardAlbum
    }
}
</script>

<style scoped lang="scss">

@import "bootstrap/dist/css/bootstrap.min.css";

.riga_cust {
    width: 80%;
    display: flex;
    justify-content: center;
}

.container {
    width: 100%;
    border: 1px solid antiquewhite;
}

</style>