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
          <li :class="elem.current ? 'active' : '' " v-for="(elem, index) in contacts" :key="index">
            <a :href="elem.url">{{ elem.nome }}</a>
          </li>
        </ul>
      </nav>
    </header>

    <!-- Main -->
    <main>
      <!-- content goes here -->
      <section>

      </section>

      <!-- links bg-blue -->
      <section>

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
          border-bottom: 3px solid rgb(8 124 236);
          a{
            color: rgb(8 124 236);
          }
        }
      }
    }
  }
  
  .container{
    width: 70%;
    margin: auto;
  }

  .active{
          border-bottom: 3px solid rgb(8 124 236);
          a{
            color: rgb(8 124 236);
          }
        }

  

</style>
