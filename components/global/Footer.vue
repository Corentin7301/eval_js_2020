<template>
  <div id="footer">
    <div class="footer-col">
      <div class="items">

      <nuxt-link v-for="item in items" :key="item.name" :to="item.page">{{item.name}}</nuxt-link>
      </div>
      <nuxt-link to="/"><img src="~/assets/img/visual-studio-code.svg" alt="vscode-logo"></nuxt-link>
      <div class="menu">
      <nuxt-link v-for="item in menu" :key="item.name" :to="item.page">{{item.name}}</nuxt-link>
      </div>
    </div>

  </div>
</template>

<script>
  export default {
    name: "footer",
    data() {
      return {
        items: [{
            name: 'VSCode',
            page: '/vscode'
          },
          {
            name: 'Corporation',
            page: '/corporation'
          },
          {
            name: 'CGV',
            page: '/cgv'
          }
        ],
        menu: [{
            name: 'A propos',
            page: '/about'
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
      };
    },
  };

</script>

<style lang="scss" scoped>
  #footer {
    text-align: center;
    height: 79px;
    background: #FFFFFF;
    display: flex;
    justify-content: center;
    align-items: center;

    .footer-col {
      display: flex;

      a,
      p {
        font-size: 21px;
        color: $darkGrey;
        text-decoration: inherit;
        font-family: "HelveticaNeue";
        margin: 0 15px 0 15px;

        &:hover {
          font-weight: bold;
        }
      }
    }
  }

  @media screen and (max-width: 1024px) {

    #footer {
      height: 100px;
      background: #FFFFFF;
      display: flex;
      justify-content: center;
      align-items: center;

      .footer-col {
        display: flex;

        .items,.menu {
          display: flex;
          flex-direction: column;
        }

        a,
        p {
          font-size: 21px;
          color: $darkGrey;
          text-decoration: inherit;
          font-family: "HelveticaNeue";
          margin: 0 15px 0 15px;

          &:hover {
            font-weight: bold;
          }
        }
      }
    }



  }

</style>
