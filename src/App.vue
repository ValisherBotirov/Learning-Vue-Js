<template>

 <h1>Hello vue.js):</h1>
<h2>CEO {{name}}</h2>
<input type="text" ref="name">
<button @click = "clickBtn">Click </button>
<Header name = "Valisher"/>
<Footer :cars = "cars" @hide = "hideCustomText"/>

<h2 v-if = "isOpen">{{customEventText}}</h2>
<button @click = "openCustomText">Open</button>

<p>Chackbox group</p>

<input type="checkbox"  value="man" v-model="checkValue">
<input type="checkbox"  value="woman" v-model="checkValue">

<p>{{checkValue}}</p>

<Form/>

</template>

<script>

import Header from "./components/Header.vue";
import Footer from "./components/Footer";
import Form  from "./components/Form.vue"


export default {
  name : "App",

  components : {
    Header,
    Footer,
    Form,
    },

  data() {
    return {
      name : "Valisher",
      cars : ["Malibo , Captiva , Gentra , Cobolt , Nexia"],
      customEventText : "This is custom event text",
      isOpen : false,
      checkValue : [],
    }
  },
  methods: {

    clickBtn(){
      console.log("Btn click");
      console.log(this.$refs.name.value);
      this.$refs.name.classList.add("focus");
    },

    openCustomText(){
    this.isOpen = true;
    },

    hideCustomText(){
      this.isOpen = false;
    },

    isChecked(){
      console.log(this.checkValue);
    }
    

  },
}
  </script>






<style >

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
