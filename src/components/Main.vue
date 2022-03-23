<template>
    <main>
      <div class="first-section">

        <div class="container-slide">
          <h1></h1>
        </div>
      </div>

      <div class="second-section">
        <div class="container-slide">
          <ul>
            <li v-for="category in categories" :key="category">
              <a href="#!"><span><img :src="category.img" alt="category.text"></span> {{ category.text }}</a>
            </li>
          </ul>

        </div>
      </div>
    </main>
</template>

<script>

import dcComics from '../assets/img/buy-comics-digital-comics.png';
import dcMerchandise from '../assets/img/buy-comics-merchandise.png';
import dcSubs from '../assets/img/buy-comics-subscriptions.png';
import dcShop from '../assets/img/buy-comics-shop-locator.png';
import dcVisa from '../assets/img/buy-dc-power-visa.svg';

export default {
  name: 'MainDC',
  components: {
      },

      data() {
          return {
              categories: [
                { 
                      text: "Digital comics",
                      img: dcComics,
                },

                { 
                      text: "dc merchandise",
                      img: dcMerchandise,
                },
                
                { 
                      text: "subscription",
                      img: dcSubs,
                },
                
                { 
                      text: "comic shop locator",
                      img: dcShop,
                },
                
                { 
                      text: "dc power visa",
                      img: dcVisa,
                },
            ],

          };
      }
}

</script>

<style scoped lang="scss">

@import "../temporary/preformat";
@import "../temporary/reset";
@import "../temporary/variables";

main {

  //Content
  .first-section {
    background-color: black;

    div {
      display: flex;
      align-items: center;

      &:after {
        content: "--> Content Goes Here <--";
        color: white;
        font-weight: bold;
        font-size: 1.5rem;
        }
      }
    }

    //Merchandise
    .second-section {
      background-color: $blue;

      div {
        display: flex;
        align-items: center;

        ul {
          list-style: none;
          display: flex;
          align-items: center;
        }

        li {
            display: flex;
            align-items: center;
          a {
            text-decoration: none;
            text-transform: uppercase;
            padding: 1.5rem;
            color:white;
            display: flex;
            align-items: center;

            span {
              width: 45px;
              margin-right: 1rem;

              img {
                width: 100%;
              }
            }
          }
        }
      }
    }
}

</style>