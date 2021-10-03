<template>
    <div class="album">
        <img :src="info.poster" :alt="info.author">
        <h1>{{info.title}}</h1>
        <div>{{info.author}}</div>
        <div>{{info.year}}</div>
    </div>
</template>

<script>
export default {
    name: "Album",
    props: {
        info: Object
    },
}
</script>

<style lang="scss" scoped>
    .album {
        margin-top: 20px;
        margin-right: 40px;
        text-align: center;
        color: white;
        padding: 20px;
        background-color: #2E3A46;
        width: calc((100% / 5) - 40px);
            div {
                color: #80746c;
                width: 100%;
            }

            img {
                width: 100%;
            }
    }

    h1 {
        margin: 20px 0;
    }
</style>