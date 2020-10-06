<template>
  <div class="home">
        <h1>{{ message }}</h1>

    <button v-on:click="showJoke()">Make me laugh</button>
    <h2>{{ joke.setup }} </h2>
    <h2>{{ joke.punchline }} </h2>
    

  </div>
</template>

<style>
</style>

<script>
import axios from "axios";

export default {
  data: function () {
    return {
      message: "(APP)ropriate Jokes!",
      joke: [],
      punchline: [],
      setup: [],
    };
  },
  created: function () {},
  methods: {
    showJoke: function () {
      axios.get(`/api/jokes/3`).then((response) => {
        console.log(response);
        this.joke = response.data;
      });
    },
  },
};
</script>