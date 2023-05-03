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
  <div>
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
      <section>

      </section>

      <!-- SIGN-UP -->
      <section>

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
</style>
