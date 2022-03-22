<template>
    <footer>
      <div class="first-section">
        <div>

          <div class="container-links">
            <div v-for="nav in navigationList" :key="nav" class="link">
            <h1> {{ nav.category }}</h1>
              <ul v-for="linkNav in nav.links" :key="linkNav">
                <li>{{ linkNav.text }} </li>
              </ul>

            </div>
          </div>
        <img src="../assets/img/dc-logo-bg.png" alt="dcLogoBg" class="dclogo">
        </div>

      </div>
    </footer>
</template>

<script>

export default {
  name: 'FooterDC',

  data () {
    return {

      navigationList: [
        {
          category: "DC Comics",
          links: [
            {
              text: "Characters"
            },

            {
              text: "Comics"
            },

            {
              text: "Movies"
            },

            {
              text: "TV"
            },

            {
              text: "Games"
            },

            {
              text: "Videos"
            },

            {
              text: "News"
            },
          ],
        },

        {
          category: "Shop",
          links: [
            {
              text: "Shop DC"
            },

            {
              text: "Shop DC Collectibles"
            }
          ]
        },

        {
          category: "DC",
          links: [
            {
              text: "Terms Of Use"
            },

            {
              text: "Privacy policy (New)"
            },

            {
              text: "Ad Choices"
            },

            {
              text: "Advertising"
            },

            {
              text: "Jobs"
            },

            {
              text: "Subscriptions"
            },

            {
              text: "Talent Workshops"
            },

            {
              text: "CPSC Certificates"
            },

            {
              text: "Ratings"
            },

            {
              text: "Shop Help"
            },

            {
              text: "Contact Us"
            },
          ],
        },

                {
          category: "Sites",
          links: [
            {
              text: "DC"
            },

            {
              text: "MAD Magazine"
            },

            {
              text: "DC  Kids"
            },

            {
              text: "DC Universe"
            },

            {
              text: "DC Power Visa"
            },
          ],
        }
      ],
    };

  },

  components: {
  }
}

</script>

<style lang="scss">

@import "../temporary/preformat";
@import "../temporary/reset";
@import "../temporary/variables";


footer {

  
  .first-section {
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover;
    height: 400px;
    overflow: hidden;
    padding-top: 3rem;
    padding-left: 17vw;
    padding-right: 17vw;

    div {
      display: flex;
      justify-content: space-between;

      //Links
      .container-links {

        display: flex;
        flex-direction: column;
        align-items: flex-start;

        .link {
          display: flex;
          flex-direction: column;
          align-items: flex-start;

            h1 {
              text-transform: uppercase;
              padding-bottom: 1rem ;
            }

            ul {
              list-style: none;
              vertical-align: middle;
              padding-bottom: 1rem;

                li {
                  line-height: .2rem;
                  color: $lightgrey;
                  font-size: .8rem;

                  a  {
                    text-decoration: none;
                  }

              }
            }
          }
        }
      }

    .dclogo {
      position: relative;
       bottom: 150px;
     }


  }   
}

</style>