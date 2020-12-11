<template>
  <nuxt-link :to="url" class="buttonJoin">
    <slot />
  </nuxt-link>
</template>

<script>
  export default {
    name: "button",
    props: ['url'],

    data() {
      return {

      }
    },
  }

</script>

<style lang="scss">
  .buttonJoin {
    font-family: "HelveticaNeue";
    font-weight: lighter;
    transition: 0.2s;
    background: $blue;
    color: $white;
    font-size: 38px;
    padding: 20px 230px 20px 40px;

    &:hover {
      background-color: $white;
      color: $blue;
      transition: 0.3s;
    }
  }

  @media screen and (max-width: 1024px) {
    .buttonJoin {
      color: $white;
      font-size: 28px;
      padding: 20px 70px 20px 20px;

      &:hover {
        background-color: $white;
        color: $blue;
        transition: 0.3s;
      }
    }
  }

</style>
