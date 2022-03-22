<template>
    <header>
        <div class="container-small"></div>
        <div class="">
            <div class="container-slide">
                <img src="../assets/img/dc-logo.png" alt="Logo Dc">

                <nav>
                    <ul>
                        <li v-for="link in links" :key="link"><a href="#!">{{ link.text }}</a></li>
                    </ul>
                </nav>       
            </div>
        </div>
    </header>
</template>

<script>

export default {
    
    name: 'HeaderDC',
    components: {
      },

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
      }
}

</script>

<style lang="scss">

@import "../temporary/preformat";
@import "../temporary/reset";
@import "../temporary/variables";

header {

        div { 

            background-color: white;


        div {
            display: flex;
            justify-content: space-between;
            align-items: center;

            img {
                
                width: 80px;
            }

        
            ul {
                display: flex;
                align-items: center;
                list-style: none;


                li {
                    
                    a {
                        font-size: .9rem;
                        text-decoration: none;
                        font-weight: bold;
                        text-transform: uppercase;
                        padding: 1rem;
                        color:black
                    }
                }
            }
        }
    }
}



</style>