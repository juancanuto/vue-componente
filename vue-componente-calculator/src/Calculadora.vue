<template>
  <div id="calculadora">

    <input-numeros @sendPrimeiro="primeiro = $event" @sendSegundo="segundo = $event"></input-numeros>
    <calcula-operacoes :primeiro="this.primeiro" :segundo="this.segundo"></calcula-operacoes>
  </div>
</template>

<script>
import Input from "./components/Input.vue";
import Calcula from "./components/Calcula.vue";

export default {
  name: "calculadora",

  data() {
    return {
      primeiro: 0,
      segundo: 0
    };
  },
  components: {
    "input-numeros": Input,
    "calcula-operacoes": Calcula
  }
};
</script>

<style>
#calculadora {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
