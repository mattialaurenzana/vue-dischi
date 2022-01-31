<template>
    
        <div class="card">
            <img :src="disk.poster" alt="music disk">
            <div class="title">{{disk.title}}</div>
            <div class="author">{{disk.author}}</div>
            <span class="year">{{disk.year}}</span>
        </div>
    
</template>

<script>
export default {
    props: {
        disk: Object
    }
}
</script>

<style lang="scss" scoped>
    .card{
        background-color:  rgb(54, 65, 77);
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 10px 0;
        font-size: 11px;
        margin: 10px 10px;
        width: calc((20%) - 20px);

        img{
            width: 100px;
            height: 100px;
        }

        .title{
            font-size: 16px;
            color: white;
            text-transform: uppercase;
            max-width: 95px;
            word-break: break-word;
            text-align: center;
            margin: 5px 0;
        }

        .author, .year{
            font-size:15px;
            color: grey;
        }

    }
</style>