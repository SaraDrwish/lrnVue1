<template>
 
     <h1> {{ title}} </h1>
     <div v-if="showModal">
       <Modal  theme="saaaaaaaaale"  @close="toggleModal"  >

        <h3>hello this is a slot try title</h3>
        <p>hi this is a p Lorem ipsum dolor sit amet.</p>
        <template v-slot:links>
              <a href="#">more info</a>
        </template>
       </Modal>
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
      showModal: false,
      showModalTwo:false
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
    ,
    toggleModalTwo() {
      this.showModalTwo = !this.showModalTwo
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
