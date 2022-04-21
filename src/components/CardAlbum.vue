<template>
    <div class="card_cust">
        <img :src="poster" alt="">
        <h6>{{title}}</h6>
        <span>{{author}}</span>
        <span>{{year}}</span>
    </div>
</template>

<script>
import "bootstrap"

export default {
    name: 'CardAlbum',
    props: {
        poster: String,
        title: String,
        author: String,
        year: String
    }
}
</script>

<style scoped lang="scss">

@import "bootstrap/dist/css/bootstrap.min.css";

.card_cust {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 250px;
    padding: 20px 0;
    margin: 10px;
    flex-wrap: wrap;
    background-color: #2e3a46;
    color: white;

}

img {
    height: 150px;
    width: 150px;
}

h6 {
    display: inline;
    margin: 15px 0 5px 0;
    font-weight: bold;
    text-transform: uppercase;
}

span {
    color: grey;
}

</style>