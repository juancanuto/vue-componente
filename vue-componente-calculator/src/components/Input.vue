<template>
  <div>
    <input type="number" :value="primeiro" @input="getPrimeiroNumero" placeholder="Digite o 1º número">
    <input
      type="number"
      :value="segundo"
      @input="getSegundoNumero"
      v-on:input="$emit('input', $event.target.value)"
      placeholder="Digite o 2º número"
    >
  </div>
</template>

<script>
export default {
  name: "input",

  data: function() {
    return {
      primeiro: 0,
      segundo: 0
    };
  },
  methods: {
    getPrimeiroNumero(event) {
      this.primeiro = event.target.value;
      this.$emit("sendPrimeiro", this.primeiro);
    },

    getSegundoNumero(event) {
      this.segundo = event.target.value;
      this.$emit("sendSegundo", this.segundo);
    }
  }
};
</script>

