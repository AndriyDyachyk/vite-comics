
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
                <div class="shop_card" v-for="shop in shops">
                    <img :src="shop.icon" :alt="shop.name">
                    <p>{{shop.name}}</p>
                </div>
            </div>
        </section>
        <section id="terms_and_conditions">
            <div class="container">
                <div>
                    <ul v-for="(term, index) in terms">
                        <h4>{{term.listTitle.toUpperCase()}}</h4>
                        <li v-for="(item, index) in term.list"><a href="{{item.url}}">{{item.element}}</a></li>
                    </ul>
                </div>
                <div>
                    <img src="/dc-logo-bg.png" alt="">
                </div>
            </div>
        </section>
        <section id="contacts">
            <div class="container">
                <div><a href="">SIGN-UP NOW</a></div>
                <div>
                    <h3>FOLLOW US</h3>
                    <a :href="platform.url" v-for="(platform,index) in social">
                        <img :src="platform.icon" :alt="platform.name">
                    </a>
                </div>
            </div>
        </section>
    </footer>
</template>
<style lang="">
    
</style>