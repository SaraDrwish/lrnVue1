<template>
 
     <h1> {{ title}} </h1>
     <teleport to=".modals" v-if="showModal">
       <Modal  theme="saaaaaaaaale"  @close="toggleModal"  >
        <h3>hello this is a slot try title</h3>
        <p>hi this is a p Lorem ipsum dolor sit amet.</p>
        <template v-slot:links>
              <a href="#">more info</a>
        </template>
       </Modal>
     </teleport>

     <teleport to=".modals" v-if="showModalTwo">
         <Modal  theme="sale"  @close="toggleModalTwo"  >
          <h3>sign up here </h3>
          <p> for updats and promo codes</p>
         </Modal>
      </teleport>

       <button @click="toggleModal" >open model</button>
       <button @click="toggleModalTwo" >open model 2</button>
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
#app , .modals {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
a{
  color:unset;
  display: block;
  text-decoration: none;
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
  margin: 1%;
  cursor: pointer;
  background: #cfe7ff;
  color: #ff6c91;
  font-weight: bold;
  text-transform: capitalize;
}

</style>

