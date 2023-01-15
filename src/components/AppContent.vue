<script>
import comicsData from '../assets/data/dataComics.js'
import ComicCard from './ComicCard.vue';

export default {
    components: {
        ComicCard
    },

    data() {
        return {
            comics: comicsData
        }
    }
}
</script>

<template>
    <div class="dark">
        <div class="container">
            <div class="title">
                <h2>Comics Series </h2>
            </div>
        </div>
        <div class="container">
            <div class="comics">
                <ComicCard v-for="(item, index) in comics" :key="index" :comic="item" />
            </div>
        </div>
        <div class="button">
            <a href="/">LOAD MORE</a>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

.dark {
    background-color: rgb(19, 24, 24);
}

.title {
    position: relative;


    h2 {
        background-color: $blue;
        width: 250px;
        padding: 10px;
        text-align: center;
        position: absolute;
        top: -20px;
        color: $white;
    }
}

.comics {
    @include center;
    justify-content: space-between;
    padding-top: 100px;
}

.button {
    padding: 20px 0;
    display: flex;
    justify-content: center;


    a {
        background-color: $blue;
        padding: 10px;
        text-align: center;
        color: $white;
        text-decoration: none;
        margin-bottom: 20px;
    }

}
</style>