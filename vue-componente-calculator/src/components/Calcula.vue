<template>
  <div>
    <p>{{primeiro}} * {{segundo}} = {{primeiro * segundo}}</p>
    <p>{{primeiro}} - {{segundo}} = {{primeiro - segundo}}</p>
    <p>{{primeiro}} + {{segundo}} = {{Number(primeiro) + Number(segundo)}}</p>
  </div>
</template>

<script>

export default {
  props: {
    primeiro: Number,
    segundo: Number
  }
};
</script>

<style>
</style>

