<script>
  export default{
    // name: "",
    data(){
      return{
          contacts: [
              {
                nome: 'Characters',
                url: '/Characters',
                current: false,
              },
              {
                nome: 'Comics',
                url: '/Comics',
                current: true,
              },
              {
                nome: 'Movies',
                url: '/Movies',
                current: false,
              },
              {
                nome: 'TV',
                url: '/TV',
                current: false,
              },
              {
                nome: 'Games',
                url: '/Games',
                current: false,
              },
              {
                nome: 'Collectibles',
                url: '/Collectibles',
                current: false,
              },
              {
                nome: 'Videos',
                url: '/Videos',
                current: false,
              },
              {
                nome: 'Fans',
                url: '/Fans',
                current: false,
              },
              {
                nome: 'News',
                url: '/News',
                current: false,
              },
              {
                nome: 'Shop',
                url: '/Shop',
                current: false,
              },

          ]
      }
    }
  }
</script>

<template>
  <div id="tutto">
    <!-- header -->
    <header>
      <!-- navbar -->
      <nav class="container">
        <img src="./assets/img/dc-logo.png" alt="logo-small">
        <ul>
          <li :class="elem.current ? 'active-nav' : '' " v-for="(elem, index) in contacts" :key="index">
            <a :href="elem.url">{{ elem.nome }}</a>
          </li>
        </ul>
      </nav>
    </header>

    <!-- Main -->
    <main>
      <!-- content goes here -->
      <section id="content-goes-here">
        <div class="container">
          <h1> -- content goes here -- </h1>
        </div>
      </section>

      <!-- links bg-blue -->
      <section id="links-DC">
        <div class="container">
          <ul>
            <li>
              <img src="./assets/img/buy-comics-digital-comics.png" alt="">
              <a href="/">DIGITAL COMICS</a>
            </li>
            <li>
              <img src="./assets/img/buy-comics-merchandise.png" alt="">
              <a href="/">DC MERCHANDISE</a>
            </li>
            <li>
              <img src="./assets/img/buy-comics-subscriptions.png" alt="">
              <a href="/">SUBSCRUBTION</a>
            </li>
            <li>
              <img src="./assets/img/buy-comics-shop-locator.png" alt="">
              <a href="/">COMIC SHOP LOCATOR</a>
            </li>
            <li>
              <img src="./assets/img/buy-dc-power-visa.svg" alt="">
              <a href="/">DC POWER VISA</a>
            </li>
          </ul>
        </div>
      </section>
    </main>

    <!-- footer -->
    <footer>
      <!-- all links -->
      <section id="all-links">
        <div class="container">
          <div>
            <ul>
              <h2>DC COMICS</h2>
              <li>
                <a href="/">Characters</a>
              </li>
              <li>
                <a href="/">Comics</a>
              </li>
              <li>
                <a href="/">Movies</a>
              </li>
              <li>
                <a href="/">TV</a>
              </li>
              <li>
                <a href="/">Games</a>
              </li>
              <li>
                <a href="/">Videos</a>
              </li>
              <li>
                <a href="/">News</a>
              </li>

              <h2>SHOP</h2>
              <li>
                <a href="/">Shop DC</a>
              </li>
              <li>
                <a href="/">Shop DC Collectibles</a>
              </li>
            </ul>
            <ul>
              <h2>DC</h2>
              <li>
                <a href="/">Terms Of Use</a>
              </li>
              <li>
                <a href="/">Privacy policy (new)</a>
              </li>
              
            </ul>
            <ul>
              <h2>SITES</h2>
              <li>
                <a href="/">DC</a>
              </li>
              <li>
                <a href="/">MAD Magazine</a>
              </li>
              <li>
                <a href="/">DC Kids</a>
              </li>
              <li>
                <a href="/">DC Universe</a>
              </li>
              <li>
                <a href="/">DC Power Visa</a>
              </li>
            </ul>
          </div>
          <img src="./assets/img/dc-logo-bg.png" alt="logo-bg">
        </div>
      </section>

      <!-- SIGN-UP -->
      <section id="sign-up">
        <div id="sign-up-c" class="container">
          <div>
            <button>SIGN-UP NOW!</button>
          </div>

          <div>
            <ul>
              <h2>FOLLOW US</h2>
              <li>
                <img src="./assets/img/footer-facebook.png" alt="">
              </li>
              <li>
                <img src="./assets/img/footer-twitter.png" alt="">
              </li>
              <li>
                <img src="./assets/img/footer-youtube.png" alt="">
              </li>
              <li>
                <img src="./assets/img/footer-pinterest.png" alt="">
              </li>
              <li>
                <img src="./assets/img/footer-periscope.png" alt="">
              </li>
            </ul>
          </div>
        </div>
      </section>
    </footer>
  </div>
</template>

<style lang="scss" scoped>
  @use './style/main.scss' as *;

  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  #tutto{
    height: 100vh;
  }

  nav{
    img{
      height: 50px;
    }
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 10%;
    ul{
      display: flex;
      list-style: none;
      li{
        margin: 0 1rem;
        padding: 1rem 0;
        a{
          color: black;
          text-decoration: none;
        }
        &:hover{
          border-bottom: 3px solid $blue-DC;
          a{
            color: $blue-DC;
          }
        }
      }
    }
  }
  
  .container{
    width: 70%;
    margin: auto;
  }

  .active-nav{
          border-bottom: 3px solid $blue-DC;
          a{
            color: $blue-DC;
          }
        }

  // parte main
  #content-goes-here{
    background-color: black;
    color: white;
    padding: 1rem 0;
  }

  #links-DC{
    background-color: $blue-DC;
    div{
      img{
      height: 30px;
      }
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 10%;
      ul{
        display: flex;
        list-style: none;
        li{
          display: flex;
          align-items: center;
          margin: 0 1rem;
          padding: 1rem 0;
          font-size: small;
          a{
            margin: 0 1rem;
            color: white;
            text-decoration: none;
          }
          }
        }
    }
  }

  // parte footer
  #all-links{
    background-image: url(./assets/img/footer-bg.jpg);
    background-size: cover;
    padding: 1rem 0;
    .container{
      display: flex;
      justify-content: space-between;
      img{
        width: 300px;
      }
      div{
        display: flex;
        ul{
        list-style: none;
        color: white;
        margin: 0 1rem;
        li{
          padding: 0.25rem 0;
          font-size: small;
          a{
            color: gray;
            text-decoration: none;
          }
          }
        }
      }
    }
  }

  #sign-up{
    background-color: rgb(48 48 48);
    padding: 1rem 0;
    #sign-up-c{
      display: flex;
      justify-content: space-between;
      button{
        background-color: rgb(48 48 48);
        color: white;
        padding: 0.5rem;
        border: 2px solid $blue-DC;
      }
      ul{
        display: flex;
        align-items: center;
        list-style: none;
        color: $blue-DC;
        h2{
          margin: 0 1rem;
        }
        li{
          display: flex;
          align-items: center;
          margin: 0 0.5rem;
        }
      }
    }
  }
</style>
