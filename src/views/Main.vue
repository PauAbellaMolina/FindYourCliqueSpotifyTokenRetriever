<template>
  <div id="home" class="d-flex flex-row align-items-center">
    <div class="w-100 ml-2 d-flex flex-column align-items-center">
      <h1 class="title">Great!</h1>
      <span class="subtitle mb-3 text-center w-50">Send the code below to the <span class="specialTS">FindYourClique Bot</span> on Telegram.</span>
      <b-input-group class="d-flex justify-content-center">
        <b-form-input class="col-md-4" v-model="this.access_token" disabled></b-form-input>
        <b-input-group-append>
          <b-button variant="dark"><b-icon icon="clipboard"></b-icon></b-button>
        </b-input-group-append>
      </b-input-group>
    </div>
  </div>
</template>

<script>

  export default {
    name: "Main",
    data() {
      return {
        access_token: "",
      }
    },
    beforeMount() {
      this.getAccessToken();
    },
    methods: {
      getAccessToken() {
        const queryString = window.location.hash;
        let access_token = queryString.substr(0, queryString.indexOf('&token_type=')).substr(queryString.indexOf('=')+1);

        this.access_token = access_token;
      }
    }
  }
</script>