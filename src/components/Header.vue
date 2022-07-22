<template>
  <div>
    <h1>Header components</h1>
    <h2>{{name}}</h2>
  </div>
</template>

<script>
  // import "../style/header.css";

  export default {
    props : ["name"],
    name  : "Header",

  }

</script>

<style scoped>

</style>