
<!-- 
  -----------------------------------------------------------
 -->

<template>
  <!-- //event modifires .self -->
  <div class="backdrop" @click.self="closeModel"  >
    <div class="modal" :class="{ sale:theme==='sale' }">
      <slot> </slot>
      <!-- <slot>default content </slot> if we dont have anything p amd h3  in the slot in app -->
      <div class="actions">
        <slot name="links"></slot>
       </div>
 
    </div>
  </div>
</template>

<!-- 
  -----------------------------------------------------------
 -->

 <script>

 export default {

   props: [  "theme"],
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

