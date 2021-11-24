<template>
  <section class="content-container">
      <div class="container">
           <div class="boxes">
                <span class="title-section">Current series</span>
                <ul>
                    <li v-for="(item, index) in List" :key="`item-${index}`">
                        <!-- <div class="card-img">
                            <img :src="item.thumb" alt="">
                        </div>
                        <div class="text-card"> {{ item.series }}</div> -->
                        <Cards :url="item.thumb" :title="item.series" />
                    </li>
                </ul>
                <div class="button-box-2">
                  <button>
                      <a href="/">
                        Load more
                      </a>
                  </button>
                </div>
           </div>
      </div>
  </section>
</template>

<script>
import ItemsDcComics from '@/data/prodItems.js';
import Cards from '@/components/Cards.vue';

export default {
    name: 'Content',
    components: {
        Cards
    },
    data() {
        return {
            List: ItemsDcComics,
        }
    }
}
</script>

<style lang="scss" scoped>

    .content-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        color: #fff;
        background-color: #1c1c1c;
        height: 100%;
        position: relative;
        .container {
            width: 100%;
            .boxes {
                display: flex;
                flex-direction: column;
                padding-top: 2rem;
                ul {
                    display: flex;
                    flex-wrap: wrap;
                    li {
                        width: calc( 100% / 6) ;
                        list-style: none;
                        padding: 1rem;
                        transition: .3s transform ease;
                        cursor: pointer;
                        // .card-img {
                        //     height: 155px;
                        //     img {
                        //         object-fit: cover;
                        //         object-position: top;
                        //         width: 100%;
                        //         height: 100%;
                        //     }
                        // }
                        // .text-card {
                        //     color: #fff;
                        //     font-size: 0.75rem;
                        //     margin-top: 1rem;
                        //     font-weight: 300;
                        // }
                        &:hover {
                            transform: scale(1.2);
                        }
                    }
                }
            }
            .button-box-2 {
                align-self: center;
                padding: 1.5rem 0 1rem;
                button {
                    background-color: #0282f9;
                    border: none;
                    padding: 0.5rem 2.5rem;
                    font-size: 0.6rem;
                    transition: .5s background ease;
                    &:hover {
                        background-color: #fff;
                    }
                    &:hover a {
                        color: #0282f9;
                    }
                    a {
                        text-transform: uppercase;
                        font-weight: 600;
                        letter-spacing: 2px;
                        color: #fff;
                        text-decoration: none;
                        transition: .5s color ease;
                    }
                }
            }
        }
        .title-section {
                    position: absolute;
                    background-color: #0282f9;
                    padding: 0.5rem 1.1rem;
                    font-size: 1.5rem;
                    top: -20px;
                }
    }

</style>