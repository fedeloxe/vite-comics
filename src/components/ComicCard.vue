<script>
export default {
    props: {
        comic: Object
    }

}
</script>
<template>
    <div class="comics-card">
        <div class="thumb">
            <img :src="comic.thumb" :alt="comic.series">
        </div>
        <div class="comic-title">
            {{ comic.series }}
        </div>
    </div>

</template>


<style lang="scss">
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

.comics-card {
    width: calc(100% / 6 - 20px);
    margin: 10px;

    .thumb {
        img {
            width: 100%;
        }
    }

    .comic-title {
        margin: 10px 0;
        color: $white;
    }
}
</style>