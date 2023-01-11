<script>
    export default {
        data() {
            return{
                menu:[
                    {
                        label: 'CHARACTERS',
                        url: '#',
                        active:false
                    },
                    {
                        label: 'COMICS',
                        url: '#',
                        active:true
                    },
                    {
                        label: 'MOVIES',
                        url: '#',
                        active:false
                    },
                    {
                        label: 'TV',
                        url: '#',
                        active:false
                    },
                    {
                        label: 'GAMES',
                        url: '#',
                        active:false
                    },
                    {
                        label: 'COLLECTIBLES',
                        url: '#',
                        active:false
                    },
                    {
                        label: 'VIDEOS',
                        url: '#',
                        active:false
                    },
                    {
                        label: 'FANS',
                        url: '#',
                        active:false
                    },
                    {
                        label: 'NEWS',
                        url: '#',
                        active:false
                    },   {
                        label: 'SHOP',
                        url: '#',
                        active:false
                    },

                ]

            }
        }

}
</script>

<template>
    <header>
        <div class="container">
            <a href="/" class="logo">
             <img src="../assets/img/dc-logo.png" alt="logo">
            </a>
            <nav>
             <ul>
                 <li v-for="(item, index) in menu" :key="index" >
                     <a :href="item.url" :class="item.active ? 'active' : ''">
                         {{ item.label }}
                     </a>
                 </li>
             </ul>
            </nav>

        </div>
    </header>
</template>


<style lang="scss">
    @use '../styles/partials/variables' as*;
    @use '../styles/partials/mixins' as*;
    header{
        .container{
            margin-top: 20px;   
            display: flex;
            align-items: center;
            justify-content: space-between;
    
    
            ul{
                list-style:none;
                @include center;
                li a{
                    text-decoration: none;
                    padding: 10px;
                    color: $black;
                    font-weight: 700;
                    padding-bottom: 20px;
    
    
                    &.active, &:hover{
                        color: $blue;
                        border-bottom: 4px solid $blue;
                    }
                }
            }
         }

    }

</style>