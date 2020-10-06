<template>
  <div class="home">
        <h1>{{ message }}</h1>
        <p>{{ subtext }}</p>

    <button v-on:click="showJoke()">Make me laugh</button>
    <h2>{{ joke.setup }} </h2>
    <h3>{{ joke.punchline }} </h3>
    

  </div>
</template>

<style>
</style>

<script>
import axios from "axios";

export default {
  data: function () {
    return {
      message: "(APP)ropriate Jokes",
      subtext: "Click the button below to read a joke!",
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