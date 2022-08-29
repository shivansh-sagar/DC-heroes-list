<template>
  <div
    class="mt-4 text-black d-flex flex-column align-items-center justify-content-center"
  >
    
      <h1 class="h1">DC Heroes</h1>
       <img  src="https://th.bing.com/th/id/OIP.DL-XesiiZEfcnyn3D4fvVQHaHa?w=156&h=180&c=7&r=0&o=5&pid=1.7" alt=""> 
    
    <!-- <h1 v-if="isShowing" v-html="title"></h1>
  
  <h1 v-else-if="isShowing=== null">This is second title</h1>
  <h2>this is a heading</h2>
  <p>this is a paragraph</p> -->
    <span class="card m-2 align-items-center"><Count /></span>
    <Nav />
  </div>
</template>

<script>
import Nav from "./components/Nav.vue";
// import Count from './components/Count.vue';

export default {
  data() {
    return {
      // title: "<h1>This is title</h1>",
      // isShowing: true,
    };
  },
  components: {
    Nav,
  },
};
</script>

<style>
.h1 {
  color: rgb(34, 26, 26);
  font-size: 50px;
}


</style>
