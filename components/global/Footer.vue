<template>
  <div id="footer">
    <div class="footer-col">
    <nuxt-link
      v-for="item in items" 
      :key="item.name"
      :to="item.page"
      class="button"
    >{{item.name}}</nuxt-link>
   <nuxt-link to="/"><img src="~/assets/img/visual-studio-code.svg" alt="vscode-logo"></nuxt-link>
    <nuxt-link
      v-for="item in menu" 
      :key="item.name"
      :to="item.page"
      class="button"
    >{{item.name}}</nuxt-link>
    </div>

  </div>
</template>

<script>
export default {
  name: "footer",
  data() {
    return {
      items: [
          {name: 'VSCode', page: '/vscode'},
          {name: 'Corporation', page: '/corporation'},
          {name: 'CGV', page: '/cgv'}
        ],
      menu: [
          {name: 'A propos', page: '/about'},
          {name: 'Equipe', page: '/equipe'},
          {name: 'Contact', page: '/contact'}
      ]
    };
  },
};
</script>

<style lang="scss" scoped>
#footer {
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

.news {
  background-color: white;
  padding: 40px;
  border-radius: 8px;
}

.form-cta {
  color: white;
  background: #FFFFFF;
  border: none;
  padding: 8px 12px;
}

.footer-social {
  display: flex;
}
</style>
