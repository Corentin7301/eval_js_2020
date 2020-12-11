<template>
  <div class="container" id="home">
    <img src="~/assets/img/visual-studio-code_bg.svg" alt="vscode-logo" id="logoGray">
    <h1>VSCode TEAM</h1>
    <h2>Devenez un dev ninja</h2>
    <ButtonJoin url="/equipe">Rejoignez l’équipe</ButtonJoin>
    <img src="~/assets/img/vscodeWindow.png" alt="vscodeWindow" class="vscodeWindow">
  </div>
</template>

<script>
  export default {
    name: "",
    head() {
      return {
        //  string or this.XXXX
        titre: "my home",
        meta: [{
          hid: 'description',
          name: 'description',
          content: 'My home description '
        }]
      }
    }
  }

</script>


<style lang="scss">
  #home {
    background-color: $background;
    margin: 0 50px 0 250px;
    height: 1100px;
    overflow: hidden;
    z-index: 1;

    #logoGray {
      position: absolute;
      top: 49px;
      left: 395px;
      width: 805px;
      height: 809px;
      z-index: -1;
    }

h1 {
      margin-top: 100px;
      font-family: "Bison";
      font-weight: bold;
      font-size: 161px;
      color: $white;
    }

    h2 {
      font-family: "HelveticaNeueLight";
      font-size: 38px;
      color: $white;

      margin-bottom: 50px;
    }

    .vscodeWindow {
      margin-top: 200px;
      width: 100%;
    }
  }

</style>
