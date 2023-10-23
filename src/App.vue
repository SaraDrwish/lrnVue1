<template>
 
     <h1> {{ title}}</h1>
     <Modal />
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
      title:"hello vue :)"
    }
  },
  methods: {
    handleClick() {
      // console.log(this.$refs.boo)
      // this.$refs.boo.classList.add("active")
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
</style>
