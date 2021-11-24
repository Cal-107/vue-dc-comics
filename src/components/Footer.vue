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
            text: 'Characters'
          },
          {
            url: '/',
            text: 'Comics'
          },
          {
            url: '/',
            text: 'Movies'
          },
          {
            url: '/',
            text: 'Tv'
          },
          {
            url: '/',
            text: 'Games'
          },
          {
            url: '/',
            text: 'Videos'
          },
          {
            url: '/',
            text: 'News'
          }
        ],
        shopList: [
          {
            url: '/',
            text: 'Shop DC'
          },
          {
            url: '/',
            text: 'Shop DC Collectibles'
          }
        ],
        dcList: [
          {
            url: '/',
            text: 'Term of Use'
          },
          {
            url: '/',
            text: 'Privacy policy (New)'
          },
          {
            url: '/',
            text: 'Ad Choises'
          },
          {
            url: '/',
            text: 'Advertising'
          },
          {
            url: '/',
            text: 'Jobs'
          },
          {
            url: '/',
            text: 'Subscriptions'
          },
          {
            url: '/',
            text: 'Talent Workshops'
          },
          {
            url: '/',
            text: 'CPSC Certificates'
          },
          {
            url: '/',
            text: 'Ratings'
          },
          {
            url: '/',
            text: 'Shop help'
          },
          {
            url: '/',
            text: 'Contact Us'
          },
        ],
        sitesList: [
          {
            url: '/',
            text: 'DC'
          },
          {
            url: '/',
            text: 'MAD Magazine'
          },
          {
            url: '/',
            text: 'DC kids'
          },
          {
            url: '/',
            text: 'DC universe'
          },
          {
            url: '/',
            text: 'DC Power Visa'
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
              font-weight: 300;
              margin: 0.1rem 0;
              text-transform: none;
              a {
                font-size: 0.80rem;
                color: rgb(205, 205, 205);
                text-decoration: none;
                &:hover {
                  color: #0282f9;
                }
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
           transition: .5s border ease,
                       .5s color ease;
           &:hover {
             border-color: #fff;
             color: #0282f9;
           }
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