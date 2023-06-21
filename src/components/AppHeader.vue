
<script>
export default {
    data(){
        return{
            navBarMenu:[
                {
                    text: "characters",
                    url: "",
                    active: false
                },
                {
                    text: "comics",
                    url: "",
                    active: false
                },
                {
                    text: "movies",
                    url: "",
                    active: false
                },
                {
                    text: "tv",
                    url: "",
                    active: false
                },
                {
                    text: "games",
                    url: "",
                    active: false
                },
                {
                    text: "collectibles",
                    url: "",
                    active: false
                },
                {
                    text: "videos",
                    url: "",
                    active: false
                },
                {
                    text: "fans",
                    url: "",
                    active: false
                },
                {
                    text: "news",
                    url: "",
                    active: false
                },
                {
                    text: "shop",
                    url: "",
                    active: false
                }
            ]
        }
    }
}
</script>
<template lang="">
    <header>
        <div class="container">
            <a><img src="/dc-logo.png" alt="" class="logo"></a>
            <ul>
                <li v-for="(menu, index) in navBarMenu" @mouseover="menu.active = true" @mouseout="menu.active = false" :class="[menu.active === true ? 'active' : '']" :key="index">
                    <a :href="menu.url" >
                        {{menu.text.toUpperCase()}}</a>
                </li>
            </ul>
        </div>
    </header>
</template>
<style lang="scss" scoped>
    header{
        background-color: white;
        position: fixed;
        top: 0px;
        left: 0px;
        right: 0px;
        
        .container{
            display: flex;
            justify-content: space-between;
            align-items: center;

            .logo{
                width: 60px;
            }

            ul{
                li{
                    display: inline-block;
                    padding: 33px 10px;
                    font-size: 13px;
                    font-weight: bold;
                    border-bottom: 4px solid white;

                    a{
                        color: black;
                    }
                }
                .active{
                    a{
                        color: rgb(2, 130, 249);
                    }
                    border-bottom-color: rgb(2, 130, 249);
                }
            }
        }
    }
</style>