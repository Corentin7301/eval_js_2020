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

    #logoBlue {
      position: absolute;
      top: 18px;
      left: 84px;
      width: 145px;
      height: 145px;
    }
  }

</style>
