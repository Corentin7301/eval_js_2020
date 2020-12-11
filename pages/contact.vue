<template>
  <div class="contact">
    <h1>Contactez-nous !! 🤘🏼</h1>
    <form action="">
      <label for="nom"></label>
      <input type="text" v-model="nom" placeholder="Nom">
      <label for="prenom"></label>
      <input type="text" v-model="prenom" placeholder="Prénom">
      <label for="email"></label>
      <input type="email" v-model="email" placeholder="Email">
      <textarea name="" id="" placeholder="Demande"></textarea>
      <ButtonJoin url="#" class="SendButton">Envoyer</ButtonJoin>
    </form>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        email: '',
        password: '',
        firstName: '',
        age: 0
      }
    },
  }

</script>

<style lang="scss">
  .contact {
    margin-left: 100px;

    h1 {
      margin: 100px 0 30px 0;
      font-family: "Bison";
      font-weight: bold;
      font-size: 161px;
      color: $white;
    }

    form {
      display: flex;
      flex-direction: column;

      input {
          font-family: "Bison";
        width: 500px;
        height: 150px;
        border-radius: 5px;
        border: none;
        margin-bottom: 20px;
        font-size: 40px;
        padding-left: 20px;
      }
      textarea {
        font-family: "Bison";
        width: 500px;
        height: 150px;
        border-radius: 5px;
        border: none;
        margin-bottom: 20px;
        font-size: 20px;
        padding-left: 20px;
      }
    }
    .SendButton {
      margin-bottom: 50px;
    }
  }

</style>
