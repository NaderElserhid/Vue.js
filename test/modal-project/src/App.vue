<template>
  <h1>{{ title }}</h1>
  <p>welcome</p>
  <div v-if="showModal">
    <Modal  theme="sale" @close="handleClick"> 
      <template v-slot:lisks>
         <a href="#">Sing up</a>
         <a href="#">more info</a>
      </template>
      <h1>Ninge Giveway!</h1>
      <p>Grap your ninja awag for half price!</p>
    </Modal>
  </div>
  <button @click="handleClick">opan modal</button>
  </template>

<script >
import Modal from './components/Modal.vue';

export default {
name: 'app',
components: {Modal},
data(){
  return{
    title : 'my First vue App :)',
    showModal : false,
  }
},
methods:{
  handleClick(){
    this.showModal = !this.showModal
  },
}
}
</script>

<style >
#app {
  font-family: Arial, Helvetica, Arial, sans-serif;
 text-align: center;
 color: #2c3e50;
 margin-top: 60px;
}
h1{
  display: inline-block;
  border-bottom: 1px solid #ddd;
  padding-bottom: 10px;
}
a{
  padding: 5px;
color: #ddd;
}

</style>
