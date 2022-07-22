<template>
  <div>
    <h1>{{name}}</h1>
    <ul>
      <li v-for="car in cars" :key="car">{{car}}</li>
    </ul>
    <button @click = "hideText">Hide</button>
  </div>
</template>

<script>
  export default {
    props : ["cars"],
    data() {
      return {
        name : "Footer components"
      }
    },
    methods: {
      hideText(){
        this.$emit("hide");
      }
    },
  }  
</script>