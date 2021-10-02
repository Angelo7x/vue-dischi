<template>
    <section>
        <div class="albums-container">
            <Album/>
            <Album/>
            <Album/>
            <Album/>
            <Album/>

        </div>
    </section>
</template>

<script>
import Album from "./Album.vue"
export default {
    name: "Albums",
    components: {
        Album
    }
}
</script>

<style lang="scss" scoped>
section {
    height: 100vh;
    background-color: #1E2D3B;
}

.albums-container {
    width: 70%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;

}

</style>