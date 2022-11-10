<script>

  export default {
    data : () => ({
      contador: 1,
    }),

    methods:{
      saludar(){
        console.log("hola")
      },
      incrementar(){
        this.contador++;
      },
      disminuir(){
        this.contador--;
      },
      reset(){
        this.contador = 1;
      }
    }
  };
    
</script>


<template>
  <div class="container">
    <img src="./assets/logo.svg" alt="logo vue" width="125" height="125">
    <!-- <img src={{logo}} alt="logo vue"> -->
    <small>
      <h1>HOLA MUNDO DESDE VUE.JS</h1>
    </small>
    <hr/>

    <h2>CONTADOR: {{ contador }}</h2>
    <!-- <button v-on:click="saludar">+1</button> -->
    <button @click="incrementar()">+1</button>
    <button @click="disminuir">-1</button>
    <button @click="reset">Reset</button>
  </div>
</template>


<style scoped>

/* @import "./assets/base.css"; */
.container{
  text-align: center;
  /* background-color: #ddd; */
}

h1 {
  /* color: red; */
  font-weight: bolder;
}

small {
  color: #666;
}

h2 {
  font-size: 2.5rem;
}

button {
  cursor: pointer;
  font-size: 1.5rem;
  margin: 0px 6px;
}

</style>