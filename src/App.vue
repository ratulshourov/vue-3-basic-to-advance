<template>
  <div>
    <app-logic></app-logic>
  
    {{name}}
    <h1 v-text="phone"></h1>
    <div v-html="title"></div>
    <h2 v-bind:class="[flag&&'stock','stockout']">SLOCK LIST /SLOCK OUT  BY ARRAY CLASS</h2>
    <h2 v-bind:class="{
      isActive,
      flag:!newCustomer,'active':'notActive'
    }">SLOCK LIST /SLOCK OUT  BY Object CLASS</h2>
    <button v-bind:disabled="disableButton">Add</button>
    <h1 v-bind:id="idname">Heading</h1>
    <h1 v-bind:class="disableButton && 'notActive'">Active Class</h1>
    <h1 v-bind:class="flag ? 'active':'notActive'">Flag Check</h1>
    <!--inline css example object and array -->

    <h2 v-bind:style="{
      background:'red',
      fontSize:'100px',
    }">inline css example  using object</h2>

    <!---->
<!---->
  </div>
 
</template>

<script>
import LogicComponent from './components/LogicComponent'

export default {
  name: 'App',
  components: {
    'app-logic':LogicComponent
  },
  data() {
    return {
      name: 'ratul',
      phone:12344,
      title:`<h1>PRACTICE</h1>`,
      disableButton:true,
      idname:'main',
      flag:false,
      isActive:false,
      newCustomer:true
    };
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
 
  color: #2c3e50;
  margin-top: 60px;
}

.active {
  color: green;
}
.notActive {
  color: red;
}

.stock {
  font-style: italic;
}

.stockout{
  background: yellow;
}
</style>
