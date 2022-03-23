<template>
  <header>
    <div>
      <div class="container-slide">
        <img src="../assets/img/dc-logo.png" alt="Logo Dc" />

        <nav>
          <ul>
            <li v-for="link in links" :key="link">
              <a href="#!">{{ link.text }}</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderDC",
  components: {},

  data() {
    return {
      links: [
        {
          text: "characters",
        },

        {
          text: "comics",
        },

        {
          text: "movies",
        },

        {
          text: "tv",
        },

        {
          text: "games",
        },

        {
          text: "collectibles",
        },

        {
          text: "video",
        },

        {
          text: "fans",
        },

        {
          text: "news",
        },

        {
          text: "shop",
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

header {
  div {
    height: 100%;
    background-color: white;

    div {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 100%;

      img {
        width: 80px;
      }

      nav {
        height: 100%;
      }

      ul {
        display: flex;
        align-items: center;
        list-style: none;
        height: 100%;

        li {
          display: flex;
          align-items: center;
          height: 100%;
          text-align: center;
          padding: 10px;

          a {
            font-size: 0.9rem;
            text-decoration: none;
            font-weight: bold;
            text-transform: uppercase;
            color: black;
          }
        }

        li:hover {
          border-bottom: 3px $blue solid;
          margin-bottom: -3px;
        }
      }
    }
  }
}
</style>
