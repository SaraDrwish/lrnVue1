<template>
 
     <h1> {{ title}} </h1>
     <div v-if="showModal">
       <Modal :header="header"  :text="text" theme="saaaaaaaaale"  @close="toggleModal"  />
     </div>
     <button @click="toggleModal" >open model</button>
 </template>

<script>

import Modal from './components/Modal.vue'

 export default {
  name: 'App',
  components: {
    Modal
  },
  data() {
    return {
      title: "hello vue :)",
      header: "this is a prop header ",
      text: "txt prop",
      showModal: false
     }
  },
  methods: {
    handleClick() {
      // console.log(this.$refs.boo)
      // this.$refs.boo.classList.add("active")
    }
    ,
    toggleModal() {
      this.showModal = !this.showModal
    }
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
h1{
  color: #92b0cd;
  font-weight: bolder;
  border-bottom: 4px rgb(139, 46, 88) solid ;
  width: 30%;
  margin: 2% auto;
  padding: 2%;
}
button{
  border: none;
  padding: 1%;
  cursor: pointer;
  background: #cfe7ff;
  color: #ff6c91;
  font-weight: bold;
  text-transform: capitalize;
}

</style>
