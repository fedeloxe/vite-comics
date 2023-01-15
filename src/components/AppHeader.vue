<script>
export default {
    data() {
        return {
            activeItem: 0,
            menu: [          //array per sezioni sito 
                {
                    label: 'CHARACTERS',
                    url: '#',
                    active: false
                },
                {
                    label: 'COMICS',
                    url: '#',
                    active: true
                },
                {
                    label: 'MOVIES',
                    url: '#',
                    active: false
                },
                {
                    label: 'TV',
                    url: '#',
                    active: false
                },
                {
                    label: 'GAMES',
                    url: '#',
                    active: false
                },
                {
                    label: 'COLLECTIBLES',
                    url: '#',
                    active: false
                },
                {
                    label: 'VIDEOS',
                    url: '#',
                    active: false
                },
                {
                    label: 'FANS',
                    url: '#',
                    active: false
                },
                {
                    label: 'NEWS',
                    url: '#',
                    active: false
                }, {
                    label: 'SHOP',
                    url: '#',
                    active: false
                },

            ]

        }
    },
    methods: {
        selectItem(index) {
            this.activeItem = index
        },
    }

}
</script>

<template>
    <header>
        <div class="container">
            <a href="/" class="logo"> <!-- logo -->
                <img src="../assets/img/dc-logo.png" alt="logo">
            </a>
            <nav> <!--lista sezioni sito -->
                <ul>
                    <li v-for="(item, index) in menu" :key="index" @click="selectItem(index)"
                        :class="(activeItem === index) ? 'active' : ''">
                        <a :href="item.url">
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

header {
    .container {
        margin-top: 20px;
        display: flex;
        align-items: center;
        justify-content: space-between;


        ul {
            list-style: none;
            @include center;


            .active {
                border-bottom: 4px solid $blue;
                padding-bottom: 20px;


            }


            li {
                border-bottom: 4px solid $white;


                a {
                    text-decoration: none;
                    padding: 10px;
                    color: $black;
                    font-weight: 700;

                }

                &.active {
                    a {
                        color: $blue;
                    }
                }

                a:hover {
                    color: $blue
                }

            }
        }
    }
}
</style>