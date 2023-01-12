<script>
export default {
    data() {
        return {
            menu: [
                {
                    img: 'buy-comics-digital-comics.png',
                    label: 'DIGITAL COMICS',
                    url: '#',
                    active: false,
                },
                {
                    img: 'buy-comics-merchandise.png',
                    label: 'DC MERCHANDISE',
                    url: '#',
                    active: true
                },
                {
                    img: 'buy-comics-subscriptions.png',
                    label: 'SUBSCRIPTION',
                    url: '#',
                    active: false
                },
                {
                    img: 'buy-comics-shop-locator.png',
                    label: 'COMIC SHOP LOCATOR',
                    url: '#',
                    active: false
                },
                {
                    img: 'buy-dc-power-visa.svg',
                    label: 'DC POWER VISA',
                    url: '#',
                    active: false
                },
            ]

        }
    },
    methods: {
        imgPath: function (img) {
            return `/src/assets/img/${img}`
        }
    }
}
</script>

<template>
    <footer>
        <div class="footer-bar"> <!--footer shop-->
            <div class="container">
                <ul>
                    <li v-for="(item, index) in menu" :key="index">
                        <a :href="item.url" :class="item.active ? 'active' : ''">
                            <img :src="imgPath(item.img)" alt=""> <span>{{ item.label }}</span>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
        <div class="footer-links"> <!--footer links-->
            <div class="container">
                <div class="col"> <!--prima colonna-->
                    <h4>DC COMICS</h4>
                    <ul>
                        <li><a href="#">Characters</a></li>
                        <li><a href="#">Comics</a></li>
                        <li><a href="#">Movies</a></li>
                        <li><a href="#">TV</a></li>
                        <li><a href="#">Games</a></li>
                        <li><a href="#">Videos</a></li>
                        <li><a href="#">News</a></li>
                    </ul>

                    <h4>SHOP</h4>
                    <ul>
                        <li><a href="#">Shop DC</a></li>
                        <li><a href="#">Shop DC Collectibles</a></li>
                    </ul>
                </div>
                <div class="col"> <!--seconda colonna-->
                    <h4>DC</h4>
                    <ul>
                        <li><a href="#">Temos Of Use</a></li>
                        <li><a href="#">Privacy policy (New)</a></li>
                        <li><a href="#">Ad Choices</a></li>
                        <li><a href="#">Advertising</a></li>
                        <li><a href="#">Jobs</a></li>
                        <li><a href="#">Subscriptions</a></li>
                        <li><a href="#">Talent Workshops</a></li>
                        <li><a href="#">CPSC Cerrificates</a></li>
                        <li><a href="#">Ratings</a></li>
                        <li><a href="#">Shop Help</a></li>
                        <li><a href="#">Contact Us</a></li>
                    </ul>

                </div>
                <div class="col"> <!--terza colonna-->
                    <h4>SITES</h4>
                    <ul>
                        <li><a href="#">DC</a></li>
                        <li><a href="#">MAD Magazine</a></li>
                        <li><a href="#">DC Kids</a></li>
                        <li><a href="#">DC Universe</a></li>
                        <li><a href="#">DC Power Visa</a></li>
                    </ul>
                </div>

            </div>
        </div>
        <div class="footer-socials"> <!--footer socials-->

        </div>
    </footer>
</template>


<style lang="scss">
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

footer {

    //footer shop 
    .footer-bar {
        background-color: $blue;
        padding: 50px;

        .container {


            //lista pagine shop 
            ul {
                list-style: none;
                @include center;
                align-items: center;

                li a {
                    text-decoration: none;
                    padding: 10px;
                    color: $white;
                    font-weight: 700;
                    padding: 0 30px;
                    display: flex;
                    align-items: center;

                    //icone shop page
                    img {
                        width: 50px;
                        padding-right: 5px;
                    }
                }
            }
        }
    }

    //liste link 
    .footer-links {
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;

        .container {
            background-image: url(../assets/img/dc-logo-bg.png);
            height: 100%;
            background-repeat: no-repeat;
            background-position: right 10% bottom 45%;
            display: flex;
            padding: 30px 0;

            .col {
                padding-right: 30px;
            }

            h4 {
                font-size: large;
                color: $white;
                padding: 15px 0;
            }

            ul {
                list-style: none;
                padding: 0;

                li {
                    padding-bottom: 10px;
                }

                li a {
                    text-decoration: none;
                    color: $grey;
                }
            }
        }
    }

}
</style>