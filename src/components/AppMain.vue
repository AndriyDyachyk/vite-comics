
<script>
import comicsDatabase from '../assets/dc-comics.json'
export default {
    data(){
        return{
            comics: comicsDatabase
        }
    }
}
</script>
<template lang="">
    <main>
        <div id="jumbotron">

        </div>
        <div class="container">
            <div class="section_label label">
                <h2>CURRENT SERIES</h2>
            </div>
            <div class="content">
                <div class="comic" v-for="(comic, index) in comics" :key="index">
                    <div class="cover">
                        <img :src="comic.thumb" :alt="comic.series">
                    </div>
                    <h5>{{comic.series.toUpperCase()}}</h5>
                </div>
            </div>
            <div class="center">
                <button class="label">LOAD MORE</button>
            </div>
        </div>
    </main>
</template>
<style lang="scss" scoped>
    main{
        background-color: rgb(28, 28, 28);
        color: white;
        margin-top: 85px;
        padding-bottom: 20px;
    }
    #jumbotron{
        width: 100%;
        height: 500px;
        background: url("/jumbotron.jpg");
        background-repeat: no-repeat;
        background-size: cover;
    }
    .section_label{
        position: relative;
        top: -20px;
        left: 0px;
        display: inline-block;
    }
    .label{
        background-color: rgb(2, 130, 249);
        padding: 5px 30px;
        min-width: 150px;
        width: fit-content;
        height: fit-content;
        border: none;
        color: white;
        margin: 0 auto;

    }
    .center{
        display: flex;
    }
    .content{
        display: flex;
        flex-wrap: wrap;
    }
    .comic{
        width: calc(100% / 6 - 20px);
        margin: 0px 10px 50px;
    }
    .cover{
        height: calc(1200px / 6 - 20px);
        overflow: hidden;
        margin-bottom: 20px;
    }
    .cover img{
        width: 100%;
        height: auto;
    }

</style>