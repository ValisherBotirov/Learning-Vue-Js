<template>
  <h1>Form components</h1>
  <form @submit = "formSubmit"> 
    <input type="text"  @keyup = "getName" placeholder = "Name" v-model = "name">
    <input type="email" placeholder = "Email" v-model="email">
    <input type="password" placeholder = "Password" v-model = "password">
    <button type="submit">Submit</button>
    <p>{{name}}</p>
    <p>{{email}}</p>
    <p>{{password}}</p>
  </form>
</template>

<script>

// import "../style/form.css";

  export default {
    name : "Form",

    components:{

    },

    data() {
      return {
        name : "",
        email : "",
        password : "",
      }
    },

    methods: {
      getName(e){
        // this.name = e.key;
      },

      formSubmit(e){
        e.preventDefault();
        let data ={
          name : this.name,
          email : this.email,
          password : this.password
        };
        console.log(data);
      }
    },
  }
</script>

<style scoped>
h1{
  color : red;
}
</style>