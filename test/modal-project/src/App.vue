<template>

  <h1>{{ title }}</h1>
  <p>welcome</p>

  <div v-if="showModalOne">
    <Modal  theme="" @close="openMadalOne"> 
      <template v-slot:links>
        <h1>Ninge Giveway!</h1>
        <p>Grap your ninja awag for half price!</p>
         <a href="#">Sing up</a>
         <a href="#">more info</a>
      </template>
    </Modal>
  </div>
   
  <div v-if="showModalTwo">
    <Modal  theme="" @close="openMadalTwo">
    <template v-slot:info>
      <h1>welcom to Model number 2</h1>
      <a href="#">Read More about us</a>
    </template>
    <h1>hello from the other Modal</h1>
    <p>Grap your ninja awag for half price!</p>
</Modal>
  </div>


  <button @click="openMadalOne">opan modal one </button>
  <button @click="openMadalTwo">opan modal two</button>

  </template>
<script>
import Modal from './components/Modal.vue';

export default {
name: 'app',
components: {Modal},
data(){
  return{
    title : 'my First vue App :)',
    showModalOne : false,
    showModalTwo : false,
  }
},
methods:{
  openMadalOne(){
    this.showModalOne = !this.showModalOne
  },
  openMadalTwo(){
    this.showModalTwo = !this.showModalTwo
  },
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
button {
  background: #bbb;
  padding: 10px;
  border: none;
  border-radius: 4px;
  margin: 10px;
  font-size: 16px;
  color: #333;
}
</style>
