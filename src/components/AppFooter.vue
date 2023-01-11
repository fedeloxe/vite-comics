<script>
    export default {
        data() {
            return{
                menu:[
                    {
                        img:'buy-comics-digital-comics.png',
                        label: 'DIGITAL COMICS',
                        url: '#',
                        active:false,
                    },
                    {
                        img:'buy-comics-merchandise.png',
                        label: 'DC MERCHANDISE',
                        url: '#',
                        active:true
                    },
                    {
                        img:'buy-comics-subscriptions.png',
                        label: 'SUBSCRIPTION',
                        url: '#',
                        active:false
                    },
                    {
                        img:'buy-comics-shop-locator.png',
                        label: 'COMIC SHOP LOCATOR',
                        url: '#',
                        active:false
                    },
                    {
                        img:'buy-dc-power-visa.svg',
                        label: 'DC POWER VISA',
                        url: '#',
                        active:false
                    },
                ]

            }
        },
        methods:{
            imgPath: function(img){
                return  `/src/assets/img/${img}`
            }
        }
    }
</script>

<template>
    <footer>
        <div class="footer-bar">
            <div class="container">
                <ul>
                    <li v-for="(item, index) in menu" :key="index" >
                        <a :href="item.url" :class="item.active ? 'active' : ''">
                            <img :src="imgPath(item.img)" alt=""> <span>{{ item.label }}</span>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>


<style lang="scss">
    @use '../styles/partials/variables' as*;
    @use '../styles/partials/mixins' as*;

    .footer-bar{
        background-color: $blue;
        padding: 50px;
        
        .container{   
    
    
            ul{
                list-style:none;
                @include center;
                align-items: center;

                li a{
                    text-decoration: none;
                    padding: 10px;
                    color: $white;
                    font-weight: 700;
                    padding: 0 30px;
                    display: flex;
                    align-items: center;
                    img{
                        width: 50px;
                        padding-right: 5px;
                    }
        
                }
                
            }
         }
        
    }
</style>