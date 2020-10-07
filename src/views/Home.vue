<template>
  <div class="home">
      <header class="masthead">
            <div class="container h-100">
                <div class="row h-100 align-items-center justify-content-center text-center">
                    <div class="col-lg-10 align-self-end">
                        <h1 class="text-lowercase text-white font-weight-bold">(app)ropriate Jokes</h1>
                        <hr class="divider my-4" />
                    </div>
                    <div class="col-lg-8 align-self-baseline">
                        <p class="text-white-75 font-weight-light mb-5">Click to hear the joke.</p>
                        <a class="btn btn-primary btn-xl js-scroll-trigger" v-on:click="showJoke()" href="#about">Make Me Laugh</a>
                      <div>
                        <p class="text-white-75 font-weight-light mb-34">{{ joke.setup }} </p>
                        <p class="text-white-75 font-weight-light mb-34">{{ joke.punchline }}</p>
                      </div>

                    </div>
                </div>
            </div>
        </header>
        <h1>{{ message }}</h1>
        <p>{{ subtext }}</p>

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