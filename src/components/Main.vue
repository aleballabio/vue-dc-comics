<template>
  <main>
    <div class="first-section">
      <!-- Jumbo -->
      <div class="jumbo">
        <img src="../assets/img/jumbotron.jpg" alt="Jumbo" />
      </div>
      <!-- Cards -->
      <div class="container-slide-noheight">
        <h1 class="current-series">Current Series</h1>

        <div class="container-cards">
          <CardsDC
            v-for="card in cards"
            :key="card.series"
            :cardSrc="card.thumb"
            :cardTitle="card.series"
            :cardType="card.type"
            :cardPrice="card.price"
          />
        </div>

        <div class="cont-load-more">
          <button class="load-more">Load More</button>
        </div>
      </div>
    </div>

    <div class="second-section">
      <div class="container-slide">
        <ul>
          <li v-for="category in categories" :key="category">
            <a href="#!">
              <span><img :src="category.img" alt="category.text" /></span>
              {{ category.text }}
            </a>
          </li>
        </ul>
      </div>
    </div>
  </main>
</template>

<script>
import dcComics from "../assets/img/buy-comics-digital-comics.png";
import dcMerchandise from "../assets/img/buy-comics-merchandise.png";
import dcSubs from "../assets/img/buy-comics-subscriptions.png";
import dcShop from "../assets/img/buy-comics-shop-locator.png";
import dcVisa from "../assets/img/buy-dc-power-visa.svg";
import CardsDC from "./CardsDC.vue";

export default {
  name: "MainDC",
  components: {
    CardsDC,
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

      cards: [
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },
};
</script>



<style scoped lang="scss">
@import "../temporary/preformat";
@import "../temporary/reset";
@import "../temporary/variables";

main {
  //Content
  .first-section {
    background-color: black;

    //Jumbo
    .jumbo {
      height: 420px;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
      }
    }

    //Cards

    .current-series {
      display: inline-block;
      background-color: $blue;
      padding: 0.8rem 1.4rem;
      text-transform: uppercase;
      position: relative;
      top: -25px;
    }

    .container-cards {
      display: flex;
      flex-wrap: wrap;
      padding-bottom: 10px;
      padding-bottom: 2rem;
      width: 100%;
    }

    .cont-load-more {
      text-align: center;
      padding-bottom: 2rem;

      .load-more {
        background-color: $blue;
        border: none;
        color: white;
        font-weight: bold;

        font-size: 0.9rem;
        text-transform: uppercase;
        padding: 1rem 4rem;
      }
    }
  }

  //Merchandise
  .second-section {
    background-color: $blue;

    div {
      display: flex;
      align-items: center;
      padding-left: 1rem;
      padding-right: 1rem;

      ul {
        flex-grow: 1;
        list-style: none;
        display: flex;
        align-items: center;
      }

      li {
        flex-grow: 1;
        display: flex;
        align-items: center;

        a {
          text-decoration: none;
          text-transform: uppercase;
          padding: 1.5rem;
          color: white;
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
