<template>
  <div id="home" class="d-flex flex-row align-items-center">
    <div class="w-100 ml-2 d-flex flex-column align-items-center">
      <h1 class="title">FindYourClique</h1>
      <h1 class="subtitle mt-3 text-center">Please, log in to <span class="specialTS">Spotify</span></h1>
      <button class="w-75 mt-2 subtitle homeBtn" v-on:click="loginSpotify">Spotify Log In</button>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Home",
    methods: {
      loginSpotify() {
        /* DEV */
        window.location.href = "https://accounts.spotify.com/authorize?client_id=a432d4cd207345bf9bbb9be8b773571b&redirect_uri=http://localhost:8080&scope=user-top-read&response_type=token";
        /* PROD */
        // window.location.href = "https://accounts.spotify.com/authorize?client_id=a432d4cd207345bf9bbb9be8b773571b&redirect_uri=https://instafy.me&scope=user-top-read&response_type=token";
      }

    }
  };
</script>
