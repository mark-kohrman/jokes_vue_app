<template>
  <div class="home">
      <header class="masthead">
            <div class="container h-100">
                <div class="row h-100 align-items-center justify-content-center text-center">
                    <div class="col-lg-10 align-self-end">
                        <h1 class="text-lowercase text-white font-weight-bold">(app)ropriate jokes</h1>
                        <hr class="divider my-4" />
                    </div>
                    <div class="col-lg-8 align-self-baseline">
                        <p class="text-white-75 font-weight-light mb-5">Click to hear the joke</p>
                        <a class="btn btn-primary btn-xl js-scroll-trigger" v-on:click="showJoke()">Joke me   </a>
                    
                      <div class="container">
                        <br>
                        <h3 class="text text-white font-weight-bold">{{ joke.joke }}</h3>
                      </div>

                    </div>
                </div>
            </div>
        </header>
  </div>
</template>

<style>
</style>

<script>
import axios from "axios";

export default {
  data: function () {
    return {
      message: "(app)ropriate jokes",
      subtext: "Click the button below to read a joke!",
      joke: [],
    };
  },
  created: function () {},
  methods: {
    showJoke: function () {
      axios.get(`/api/jokes/1`).then((response) => {
        this.joke = response.data;
      });
    },
  },
};
</script>