<template>
  <div class="index">
    <div class="home">
      <div class="home-container">
        <form class="form" @submit.prevent="onSubmit">
          <label for="perimetro">Insira aqui o perímetro</label>
          <div class="form-submit">
            <input id="perimetro" type="text" />
            <button type="submit">Enviar</button>
          </div>
        </form>
      </div>
      <div class="home-list-container">aa</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "home",
  data() {
    return {
      quotes: [],
    };
  },
  methods: {
    onSubmit() {
      fetch();
    },
  },
};
</script>


<style scoped>
* {
  box-sizing: border-box;
  font-family: Georgia, serif;
  color: #252525;
}

.index {
  background: red;
  width: 100%;
  height: 100%;
  background: url("/assets/camp.jpeg") no-repeat center;
  background-size: cover;
}

.home::before,
.home::after {
  content: "";
  display: table;
  clear: both;
}

.home {
  max-width: 960px;
  margin: 0 auto;
}

.home-container {
  max-width: 400px;
  background: crimson;
  margin: 0 auto;
}

.form {
  max-width: 500px;
}

.form-submit::after,
.form-submit::before {
  content: "";
  display: table;
  clear: both;
}

.form-submit {
  max-width: 400px;
  padding: 10px 0;
  margin: 0 5px;
}

.form label {
  font-family: Georgia, serif;
  text-transform: uppercase;
  display: block;
  margin: 0 auto;
  width: 220px;
}

.form button {
  background: #252525;
  font-family: Georgia, serif;
  text-transform: uppercase;
  cursor: pointer;
  border: none;
  float: left;
  font-size: 1.4em;
  width: 130px;
  padding: 10px;
  margin: 0 5px;
  color: #fff;
}

.form input {
  background: none;
  font-style: italic;
  font-family: Georgia, serif;
  border: 3px solid #252525;
  font-size: 1.4em;
  width: 250px;
  padding: 10px;
  float: right;
}

.home-list-container {
  max-width: 700px;
  background: rgb(165, 35, 61);
  margin: 10px auto 0 auto;
}
</style>

    <!-- <button @click="$router.push('/new')">Add Quote</button>
    <hr />
    <div class="container">
      <div class="quote" v-for="quote in quotes" :key="quote.id" :quote="quote">
        <p>
          <em>"{{quote.quote}}"</em>
          by {{quote.quote_by}}
        </p>

        <span class="added-by">added by {{quote.added_by}}</span>
      </div>
    </div> -->

  <!-- // created() {
  //   fetch("http://localhost:8000")
  //     .then((res) => res.json())
  //     .then((response) => {
  //       this.quotes = response.quotes;
  //     })
  //     .catch((e) => {
  //       console.error(e.message);
  //     });
  // }, -->
