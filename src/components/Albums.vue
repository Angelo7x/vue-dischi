<template>
    <section>
        <div class="albums-container">
            <Album v-for="(album, index) in albums" :key="index" :info="album"/>
        </div>
    </section>
</template>

<script>
import axios from "axios";
import Album from "./Album.vue"
export default {
    name: "Albums",
    components: {
        Album
    },
    data() {
        return {
            albums: []
        }
    },
    created() {
        axios
            .get("https://flynn.boolean.careers/exercises/api/array/music")
            .then( (res) => {
                this.albums = res.data.response;
            });
    }
}
</script>

<style lang="scss" scoped>
section {
    background-color: #1E2D3B;
}

.albums-container {
    width: 70%;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    // justify-content: space-between;
}

</style>