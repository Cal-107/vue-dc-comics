<template>
  <footer class="footer-section">
    <div class="sub-footer-1">
      <section class="container">
        <div class="list">
        <ul>
          <h1>Dc Comics</h1>
          <li v-for="(link,i) in DcComicsList" :key="`link-${i}`">
            <a :href="link.url">
                  {{ link.text }}
            </a>
          </li>
          <h1>Shop</h1>
          <li v-for="(link,i) in shopList" :key="`link-2-${i}`">
            <a :href="link.url">
                  {{ link.text }}
            </a>
          </li>
        </ul>

        <ul>
          <h1>Dc</h1>
          <li v-for="(link,i) in dcList" :key="`link-${i}`">
            <a :href="link.url">
                  {{ link.text }}
            </a>
          </li>
        </ul>

        <ul>
          <h1>Sites</h1>
          <li v-for="(link,i) in sitesList" :key="`link-${i}`">
            <a :href="link.url">
                  {{ link.text }}
            </a>
          </li>
        </ul>
        </div>
  
        <div class="img-box">
        </div>
      </section>
    </div>

    <div class="sub-footer-2">
      <section class="container">
        <div class="sub-footer-container">
          <div>
            <button>Sign-Up Now!</button>
          </div>
  
          <div class="social-box">
            <span>Follow us</span>
            <ul class="list-2">
              <li v-for="(social, i) in socialList" :key="`list-${i}`">
                <a href="/">
                  <img :src="social.image" :alt="social.text">
                </a>
              </li>
            </ul>
          </div>
        </div>
      </section>
    </div>
  </footer>
</template>

<script>
export default {
    name: 'Footer',
    data() {
      return {
        DcComicsList: [
          {
            url: '/',
            text: 'characters'
          },
          {
            url: '/',
            text: 'comics'
          },
          {
            url: '/',
            text: 'movies'
          },
          {
            url: '/',
            text: 'tv'
          },
          {
            url: '/',
            text: 'games'
          },
          {
            url: '/',
            text: 'videos'
          },
          {
            url: '/',
            text: 'news'
          }
        ],
        shopList: [
          {
            url: '/',
            text: 'shop dc'
          },
          {
            url: '/',
            text: 'shop dc collectibles'
          }
        ],
        dcList: [
          {
            url: '/',
            text: 'term of use'
          },
          {
            url: '/',
            text: 'Privacy policy (new)'
          },
          {
            url: '/',
            text: 'ad choises'
          },
          {
            url: '/',
            text: 'advertising'
          },
          {
            url: '/',
            text: 'jobs'
          },
          {
            url: '/',
            text: 'subscriptions'
          },
          {
            url: '/',
            text: 'talent workshops'
          },
          {
            url: '/',
            text: 'cpsc certificates'
          },
          {
            url: '/',
            text: 'ratings'
          },
          {
            url: '/',
            text: 'shop help'
          },
          {
            url: '/',
            text: 'contact us'
          },
        ],
        sitesList: [
          {
            url: '/',
            text: 'dc'
          },
          {
            url: '/',
            text: 'Mad megazine'
          },
          {
            url: '/',
            text: 'dc kids'
          },
          {
            url: '/',
            text: 'dc universe'
          },
          {
            url: '/',
            text: 'dc power visa'
          }
        ],
        socialList: [
          {
            text: 'Facebook',
            url: '/',
            image: require('@/assets/footer-facebook.png')
          },
          {
            text: 'Twitter',
            url: '/',
            image: require('@/assets/footer-twitter.png')
          },
          {
            text: 'Periscope',
            url: '/',
            image: require('@/assets/footer-periscope.png')
          },
          {
            text: 'Pinterest',
            url: '/',
            image: require('@/assets/footer-pinterest.png')
          },
          {
            text: 'You-Tube',
            url: '/',
            image: require('@/assets/footer-youtube.png')
          }
        ]
      }
    }
}
</script>

<style scoped lang="scss">

   .footer-section {
     background-image: url('../assets/footer-bg.jpg');
     background-repeat: no-repeat;
     background-size: cover;
     color: #fff;
     display: flex;
     flex-direction: column;
     height: 100%;
     .sub-footer-1 {
       height: 100%;
        .container {
          display: flex;
          justify-content: space-between;
          align-items: center;
          .img-box {
            background-image: url('../assets/dc-logo-bg.png');
            background-repeat: no-repeat;
            background-position-y: center;
            height: 500px;
            width: 50%;
          }
          .list {
            display: flex;
            width: 50%;
            
            h1 {
              font-size: 1.2rem;
              margin: 1rem 0;
            }

            ul {
              padding: 0rem 4rem 0 0;
              height: 100%;
            }

            li {
              list-style: none;
              font-weight: 400;
              margin: 0.1rem 0;
              text-transform: lowercase;
              text-transform: capitalize;
              a {
                font-size: 0.80rem;
                color: rgb(205, 205, 205);
                text-decoration: none;
              }
            }
          }
        } 
     }
   }


     .sub-footer-2{
       background-color: #303030;
       .sub-footer-container {
         display: flex;
         justify-content: space-between;
         width: 100%;
         padding: 2rem 0;
         button {
           padding: 0.5rem .6rem;
           background-color: transparent;
           border: 2px solid #0282f9;
           color: #fff;
           text-transform: uppercase;
           cursor: pointer;
         }
       }
       .social-box {
         display: flex;
         align-items: center;
         span {
           margin-right: 1rem;
           color: #0282f9;
         }
         .list-2 {
           display: flex;
           list-style: none;
           li {
             margin: 0 0.2rem;
             img {
               width: 80%;
             }
           }
         }
       }
     }


</style>