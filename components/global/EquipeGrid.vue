<template>
  <div>
    <h1>EQUIPE</h1>
    <div id="teamGrid">
      <div class="user" v-for="user in users" :key="user.id">
        <img src="~/assets/img/avatars/avatar1.png" alt="avatar" class="avatar">
        <h3 class="name">
          {{ user.name }}
        </h3>
        <div class="user-email">
          <h3 class="email">{{user.email}}</h3>

        </div>
        <nuxt-link to="https://github.com/"><img src="~/assets/img/Github.svg" alt="github" class="github"></nuxt-link>

      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "teamGrid",
    layout: "equipe",
    data() {
      return {
        users: []
      }
    },
    methods: {
      async fetchUsers() {
        const api = 'https://jsonplaceholder.typicode.com/users'
        try {
          const response = await fetch(api);
          // Vue.teamgrid.data.users = await response.json()
          this.users = await response.json()
        } catch (error) {
          console.log(error);
        }
      }
    },
    mounted() {
      this.fetchUsers()
    }
  }

</script>

<style lang="scss" scoped>
  h1 {
    width: 100%;
    text-align: center;
    font-family: "Bison";
    font-weight: bold;
    font-size: 161px;
    color: $white;
    margin-top: 20px;
  }

  #teamGrid {
    margin-top: 150px;
    width: 100%;
    display: grid;
    gap: 125px 49px;
    grid-template-columns: repeat(4, 20%);
    grid-template-rows: auto;
    justify-content: center;
  }

  .avatar {
    width: 110px;
    margin-top: -60px;
  }

  .user {
    height: 250px;
    background-color: white;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;

    &:last-child {
      margin-bottom: 50px;
    }

    .name {
      margin: 50px 0 10px 0;
      font-size: 22px;
      color: $darkGrey;
      font-family: "HelveticaNeue";
      font-weight: normal;
    }

    .email {
      margin-bottom: 30px;
      font-size: 18px;
      color: $darkGrey;
      font-family: "HelveticaNeue";
      font-weight: lighter;
    }

    .github {
      margin-top: 10px;
      transition: 0.2s;
      width: 35px;

      &:hover {
        transition: 0.3s;
        opacity: 0.8;
      }
    }
  }

  @media screen and (max-width: 1024px) {
div {
  display: flex;
  flex-direction: column;
  align-items: center;
}

    h1 {
      color: $background;
      font-size: 100px;
    }

    #teamGrid {
      width: 100%;
      grid-template-columns: repeat(1, 290px);
      margin-top: 150px;

      .user {
        background-color: $background;
        height: 320px;
      }

      .avatar {
        border: 5px solid $blue;
        box-sizing: border-box;
        border-radius: 50%;
        width: 200px;
        margin-top: -100px;
      }

      .name {
        color: $white;
        font-size: 25px;
      }

      .email {
        color: $white;
        font-size: 22px;
      }
    }
  }

</style>
