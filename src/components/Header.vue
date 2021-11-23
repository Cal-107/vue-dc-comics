<template>
    <header class="header-section">
        <!-- Logo -->
        <a href="/">
             <img src="../assets/dc-logo.png" alt="Logo DC Comics">
        </a>
        <!-- Start Nav with Link -->
        <nav>
            <ul>
                <li v-for="(link, index) in linkNav" :key="`link-${index}`"
                    :class="{active: link.activeLink}"
                >
                    <a :href="link.url">
                        {{ link.text }}
                    </a>
                </li>
            </ul>
        </nav>
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
    }
}
</script>

<style lang="scss" scoped>

    .header-section {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1rem 0.5rem;
        height: 150px;

         nav {
             height: 100%;
             ul {
                 list-style: none;
                 display: flex;
                 height: 100%;

                 li {
                     height: 100%;
                     display: flex;
                     margin: 0 .80rem;
                     border-bottom: 5px solid transparent;
                        &.active,
                        &:hover {
                            border-bottom-color: #0282f9;
                            color: #0282f9;
                        }    
                        a {
                           text-decoration: none;
                           margin: 3rem 0;
                           font-size: 0.8rem;
                       }
                    }
                }        
            }
    }

</style>