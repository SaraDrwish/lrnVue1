
<!-- 
  -----------------------------------------------------------
 -->

<template>
  <!-- //event modifires .self -->
  <div class="backdrop" @click.self="closeModel"  >
    <div class="modal" :class="{ sale:theme==='sale' }">
      <h1>{{header}}</h1>
      <p>{{text}}</p>
      <!-- <button @click="closeModel" >hide</button> -->
    </div>
  </div>
</template>

<!-- 
  -----------------------------------------------------------
 -->

 <script>

 export default {

   props: ["header", "text", "theme"],
   methods: {
      closeModel() {
       this.$emit("close")
     }
  }

  }

</script>

<!-- 
  -----------------------------------------------------------
 -->



<style scoped>

.modal{
  width: 44rem;
  height: 13rem;
  border-radius: 2rem;
  padding: 1%;
  text-align: center;
  margin: 11% auto;
  color: brown;
  background: lightgoldenrodyellow;
}
.backdrop{
  position: fixed;
  top: 0;
  background-color: rgba(143, 188, 143, 0.67);
  width: 100%;
  height: 100%;
 }
 h1{
  color: mediumturquoise;
  border: none;
 }
 .sale{
  background-color: tomato;
  color: antiquewhite;
 }


</style>


<!-- 
  -----------------------------------------------------------
 -->

