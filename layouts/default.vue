<template>
  <div>
    <Navbar />
    <Nuxt />
    <Footer />
  </div>
</template>

<style lang="scss" scoped>
  body {
    min-height: 100vh;
  }

  div {
    background-color: $background;
    position: relative;

  }
  @media screen and (max-width: 1024px) {
    body {
      div {
        max-width: 100%;
        background-color: $white;
      }
    }
  }
</style>
