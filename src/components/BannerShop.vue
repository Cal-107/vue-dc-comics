<template>
  <section class="shop-section">
      <div class="container">
          <ul>
              <li>
                <a href="/">
                  <div class="box-img">
                        <img src="../assets/buy-comics-digital-comics.png" alt="">
                  </div>
                  <div>
                      Digital Comics
                  </div>
                </a>
              </li>
              <li>
                <a href="/">
                  <div class="box-img">
                        <img src="../assets/buy-comics-merchandise.png" alt="">
                  </div>
                  <div>
                      Dc Merchandise
                  </div>
                </a>
              </li>
              <li>
                <a href="/">
                  <div class="box-img">
                        <img src="../assets/buy-comics-subscriptions.png" alt="">
                  </div>
                  <div>
                      Subscription
                  </div>
                </a>
              </li>
              <li>
                <a href="/">
                  <div class="box-img">
                        <img src="../assets/buy-comics-shop-locator.png" alt="">
                  </div>
                  <div>
                      Comic Shop Locator
                  </div>
                </a>
              </li>
              <li>
                <a href="/">
                  <div class="box-img">
                        <img src="../assets/buy-dc-power-visa.svg" alt="">
                  </div>
                  <div>
                      Dc Power Visa
                  </div>
                </a>
              </li>
          </ul>
      </div>
  </section>
</template>

<script>
export default {
    name: 'BannerShop'
}
</script>

<style lang="scss" scoped>
.shop-section {
    background-color: #0282f9;
    padding: 3rem 0;
    .container {
        ul {
            display: flex;
            li {
                list-style: none;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    text-transform: uppercase;
                    font-size: .8rem;
                    font-size: .8rem;
                    width: 100%;
                a {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    width: 100%;
                    text-decoration: none;
                    color: #fff;
                    .box-img {
                        width: 20%;
                        img {
                            width: 100%;
                        }
                        margin-right: .8rem;
                    }
                }
            }
        }
    }
}
</style>