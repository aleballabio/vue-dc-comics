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

      <div class="second-section">
        <div class="container-slide">
          <div class="sign-up">
            <button>Sign-UP Now</button>
          </div>

          <div class="social">
            <h1>Follow Us</h1>

            <div class="icons">
              <img v-for="social in socials" :key="social" :src="social.img" :alt="social.nome" class="icon-image">
            </div>
          </div>
        </div>
      </div>

      <div class="container-small"></div>
    </footer>
</template>

<script>

import Facebook from '../assets/img/footer-facebook.png';
import Twitter from '../assets/img/footer-twitter.png';
import Periscope from '../assets/img/footer-periscope.png';
import Youtube from '../assets/img/footer-youtube.png';
import Pinterest from '../assets/img/footer-pinterest.png';

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

      socials : [
        {
          nome: "Facebook",
          img: Facebook,
        },

        {
          nome: "Twitter",
          img: Twitter,
        },

        {
          nome: "Youtube",
          img: Youtube,
        },

        {
          nome: "Pinterest",
          img: Pinterest,
        },

        {
          nome: "Periscope",
          img: Periscope,
        },
      ]
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

  
  //Links
  .first-section {
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover;
    overflow: hidden;
    height: 390px;
    padding-top: 3rem;
    padding-left: 17vw;
    padding-right: 17vw;

    div {
      display: flex;
      justify-content: space-between;

      .container-links {

        display: flex;
        justify-content: column;
        align-items: flex-start;

        .link {
          display: flex;
          flex-direction: column;
          align-items: flex-start;
          padding-right: 1.5rem;

            h1 {
              text-transform: uppercase;
              padding-bottom: 1rem;
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

  //Sign Up Mail

  .second-section {
    background-color: $lightdark;

    div {
      display: flex;
      justify-content: space-between;
      align-items: center;

      .sign-up {
        button {
          border: 2px solid $blue;
          background-color: transparent;
          color: white;
          text-transform: uppercase;
          padding: .8rem;
          font-size: 1.1rem;
        }
      }

      .social {
        
        h1 {
          color: $blue;
          text-transform: uppercase;
        }

        .icon-image {
          padding-left: 1rem;

        }
      }
    }
  }

}

</style>