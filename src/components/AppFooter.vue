
<script>
export default {
    data(){
        return{
            shops:[
                {
                name: "digital comics",
                icon: "/buy-comics-digital-comics.png",
                url: ""
                },
                {
                name: "dc merchandise",
                icon: "/buy-comics-merchandise.png",
                url: ""
                },
                {
                name: "subscription",
                icon: "/buy-comics-subscriptions.png",
                url: ""
                },
                {
                name: "comci shop local",
                icon: "/buy-comics-shop-locator.png",
                url: ""
                },
                {
                name: "dc power visa",
                icon: "/buy-dc-power-visa.svg",
                url: ""
                }
            ],
            terms:[
                {
                    listTitle: "dc comics",
                    list: [
                        {
                            element: "Characters",
                            url: ""
                        },
                        {
                            element: "Comics",
                            url: ""
                        },
                        {
                            element: "Movies",
                            url: ""
                        },
                        {
                            element: "TV",
                            url: ""
                        },
                        {
                            element: "Games",
                            url: ""
                        },
                        {
                            element: "Video",
                            url: ""
                        },
                        {
                            element: "News",
                            url: ""
                        }
                    ]
                },
                {
                    listTitle: "shop",
                    list: [
                        {
                            element: "Shop DC",
                            url: ""
                        },
                        {
                            element: "Shop DC Collectibles",
                            url: ""
                        }
                    ]
                },
                {
                    listTitle: "dc",
                    list: [
                        {
                            element: "Terms Of Use",
                            url: ""
                        },
                        {
                            element: "Privacy policy (New)",
                            url: ""
                        },
                        {
                            element: "Ad Choices",
                            url: ""
                        },
                        {
                            element: "Advertising",
                            url: ""
                        },
                        {
                            element: "Jobs",
                            url: ""
                        },
                        {
                            element: "Subscriptions",
                            url: ""
                        },
                        {
                            element: "Talent Workshop",
                            url: ""
                        },
                        {
                            element: "CPSC Certificates",
                            url: ""
                        },
                        {
                            element: "Ratings",
                            url: ""
                        },
                        {
                            element: "Shop Help",
                            url: ""
                        },
                        {
                            element: "Contact Us",
                            url: ""
                        }
                    ]
                },
                {
                    listTitle: "sites",
                    list: [
                        {
                            element: "DC",
                            url: ""
                        },
                        {
                            element: "MAD Magazine",
                            url: ""
                        },
                        {
                            element: "DC Kids",
                            url: ""
                        },
                        {
                            element: "DC Universe",
                            url: ""
                        },
                        {
                            element: "DC power Visa",
                            url: ""
                        }
                    ]
                }
            ],
            social:[
                {
                    name: "Facebook",
                    icon: "/footer-facebook.png",
                    url: "https://www.facebook.com"
                },
                {
                    name: "Twitter",
                    icon: "/footer-twitter.png",
                    url: "https://www.twitter.com"
                },
                {
                    name: "You Tube",
                    icon: "/footer-youtube.png",
                    url: "https://www.youtube.com"
                },
                {
                    name: "Pinterest",
                    icon: "/footer-pinterest.png",
                    url: "https://www.pinterest.com"
                },
                {
                    name: "Periscope",
                    icon: "/footer-periscope.png",
                    url: "https://www.periscope.com"
                },
            ]
        }
    }
}
</script>
<template lang="">
    <footer>
        <section id="shops">
            <div class="container">
                <a :href="shop.url" class="shop_card" v-for="shop in shops">
                    <img :src="shop.icon" :alt="shop.name">
                    <p>{{shop.name.toUpperCase()}}</p>
                </a>
            </div>
        </section>
        <section id="terms_and_conditions">
            <div class="container">
                <div id="terms_list">
                    <ul v-for="(term, index) in terms" :key="index">
                        <h4>{{term.listTitle.toUpperCase()}}</h4>
                        <li v-for="(item, index) in term.list" :key="index"><a href="{{item.url}}">{{item.element}}</a></li>
                    </ul>
                </div>
                <div class="dc_bg">
                    <img src="/dc-logo-bg.png" alt="">
                </div>
            </div>
        </section>
        <section id="contacts">
            <div class="container">
                <a href="" id="sign_up">SIGN-UP NOW!</a>
                <div id="follow">
                    <h3>FOLLOW US</h3>
                    <a :href="platform.url" v-for="(platform,index) in social">
                        <img :src="platform.icon" :alt="platform.name">
                    </a>
                </div>
            </div>
        </section>
    </footer>
</template>
<style lang="scss" scoped>
    footer{
        background: url(/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center ;
        #shops{
            background-color: rgb(2, 130, 249);
            padding: 35px 25px;

            .container{
                display: flex;
                justify-content: space-between;  
            }
            .shop_card{
                width: calc(100% / 5 - 25px);
                display: flex;
                align-items: center;
            }
            img{
                max-width: 50px;
                max-height: 50px;
            }
            p{
                color:white;
                padding-left: 10px;
            }
        }
        #terms_and_conditions{
            height: 350px;
            padding: 20px 0px;
            overflow: hidden;
            
            .container{
                display: flex;
                justify-content: space-between;
                height: 100%;
            }
            #terms_list{
                display: flex;
                flex-wrap: wrap;
                flex-flow: column wrap;
                height: 100%;
            }
            ul{
                margin: 0px 10px;
            }
            h4{
                color: white;
                margin: 15px 0px;
            }
            a{
                color: grey;
                font-size: 12px;
            }
            a:hover{
                text-decoration: underline;
                color: white;
            }
            .dc_bg{
                height: 350px;
            }
            .dc_bg img{
                transform: translate(0px,-150px);
            }
        }
        #contacts{
            padding: 20px;
            background-color: rgb(48, 48, 48);
            #sign_up{
                border: 2px solid rgb(2, 130, 249) ;
                color: white;
            }
            .container,
            #follow{
                display: flex;
                justify-content: space-between; 
                align-items: center;
                
                h3{
                    color:rgb(2, 130, 249) ;
                    padding-right: 20px;
                }
                a{
                    padding: 10px;
                }
                img{
                    height: 30px;
                }
            }
        }
    }
</style>