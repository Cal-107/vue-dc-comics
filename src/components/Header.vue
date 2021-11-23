<template>
    <header>
        <section class="header-section container">
            <!-- Logo -->
            <a href="/">
                 <img src="../assets/dc-logo.png" alt="Logo DC Comics">
            </a>
            <!-- Start Nav with Link -->
            <nav>
                <ul>
                    <li v-for="(link, index) in linkNav" :key="`link-${index}`"
                        :class="{active: link.activeLink}"
                        @click="setActiveClick(index)"
                    >
                        <a :href="link.url">
                            {{ link.text }}
                        </a>
                    </li>
                </ul>
            </nav>
        </section>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            linkNav: [
                {
                    text: 'Characters',
                    url: '/',
                    activeLink: false
                },
                {
                    text: 'Comics',
                    url: '/',
                    activeLink: true
                },
                {
                    text: 'Movies',
                    url: '/',
                    activeLink: false
                },
                {
                    text: 'Tv',
                    url: '/',
                    activeLink: false
                },
                {
                    text: 'Games',
                    url: '/',
                    activeLink: false
                },
                {
                    text: 'Collectibles',
                    url: '/',
                    activeLink: false
                },
                {
                    text: 'Videos',
                    url: '/',
                    activeLink: false
                },
                {
                    text: 'Fans',
                    url: '/',
                    activeLink: false
                },
                {
                    text: 'News',
                    url: '/',
                    activeLink: false
                },
                {
                    text: 'Shop',
                    url: '/',
                    activeLink: false
                },
            ]
        }
    },
    methods: {
        setActiveClick(index) {
            this.linkNav.forEach((el) => {
                el.activeLink = false
            })

            if (!this.linkNav[index].activeLink){
                this.linkNav[index].activeLink = true
            }else {
                this.linkNav[index].activeLink = false
            }
        }
    }
}
</script>

<style lang="scss" scoped>

    .header-section {
        display: flex;
        justify-content: space-between;
        align-items: center;
        a {
            img {
                width: 80px;
            }
        }
         nav {
             ul {
                 list-style: none;
                 display: flex;
                 

                 li {
                     
                     display: flex;
                     margin: 0 .80rem;
                     border-bottom: 5px solid transparent;
                     transition: .5s border-bottom-color ease-out;
                        &.active,
                        &:hover {
                            border-bottom-color: #0282f9;
                            color: #0282f9;
                        }    
                        a {
                           text-decoration: none;
                           margin: 3rem 0;
                           font-size: 0.7rem;
                       }
                    }
                }        
            }
    }

</style>