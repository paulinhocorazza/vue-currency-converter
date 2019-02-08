<template>
  <div id="app">
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-12">
          <h1 class="text-center">{{ msg }}</h1>
        </div>
      </div>

      <div class="row">
        <div class="col-md-3">
          <Conversor currency1="USD" currency2="BRL"></Conversor>
        </div>
        <div class="col-md-3">
          <Conversor currency1="BRL" currency2="USD"></Conversor>
        </div>
        <div class="col-md-3">
          <Conversor currency1="CAD" currency2="BRL"></Conversor>
        </div>
        <div class="col-md-3">
          <Conversor currency1="CAD" currency2="USD"></Conversor>
        </div>
      </div>
      <br>
      <div class="row">
        <div class="col-md-3">
          <Conversor currency1="BRL" currency2="CAD"></Conversor>
        </div>
        <div class="col-md-3">
          <Conversor currency1="BRL" currency2="EUR"></Conversor>
        </div>
        <div class="col-md-3">
          <Conversor currency1="EUR" currency2="BRL"></Conversor>
        </div>
        <div class="col-md-3">
          <Conversor currency1="BRL" currency2="ARS"></Conversor>
        </div>
      </div>
      <br>
            <div class="row">
        <div class="col-md-3">
          <Conversor currency1="BRL" currency2="GBP"></Conversor>
        </div>
        <div class="col-md-3">
          <Conversor currency1="GBP" currency2="BRL"></Conversor>
        </div>
        <div class="col-md-3">
          <Conversor currency1="EUR" currency2="GBP"></Conversor>
        </div>
        <div class="col-md-3">
          <Conversor currency1="GBP" currency2="USD"></Conversor>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import Conversor from "./Conversor.vue";
  export default {
    name: 'app',
    components: {
      Conversor
    },
    data() {
      return {
        msg: 'A Currency converter made with vue.js'
      }
    }
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }

  h1,
  h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>