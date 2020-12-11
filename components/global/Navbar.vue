<template>
  <nav>
    <img src="~/assets/img/visual-studio-code_blue.svg" alt="vscode-logo" id="logoBlue">

    <nuxt-link v-for="item in items" :key="item.name" :to="item.page" class="button">
      {{item.name}}
    </nuxt-link>
  </nav>
</template>

<script>
  export default {
    name: 'Navbar',
    data() {
      return {
        items: [{
            name: 'Accueil',
            page: '/'
          },
          {
            name: 'Equipe',
            page: '/equipe'
          },
          {
            name: 'Contact',
            page: '/contact'
          }
        ]
      }
    }
  }

</script>

<style lang="scss" scoped>
  nav {
    position: sticky;
    top: 0;
    z-index: 1;
    background-color: $darkGrey;
    height: 90px;
    margin: auto;
    display: flex;
    align-items: center;
    font-family: "HelveticaNeue";
    font-weight: lighter;
    display: flex;
    align-items: center;
    justify-content: center;
    
    #logoBlue {
      position: absolute;
      top: 18px;
      left: 84px;
      width: 145px;
      height: 145px;
      z-index: 100;
    }

    a {
      text-decoration: inherit;
      color: inherit;
    }

    .button {
      color: $white;
      font-size: 22px;
      padding: 0 60px;
      height: 100%;
      display: flex;
      align-items: center;
      transition: 0.2s;
    }

    .button:hover,
    .nuxt-link-exact-active {
      background-color: $lightGrey;
      transition: 0.3s;

    }
  }

  @media screen and (max-width: 1024px) {
    nav {
      height: 90px;
      background-color: $blue;

      .button {
        padding: 0 20px;

      }

      .hover,
      .nuxt-link-exact-active {
        background-color: $white;
        color: $blue;
      }
    }
    #logoBlue {
      display: none;
    }
  }

</style>
