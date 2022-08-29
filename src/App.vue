<template>
  <button class="btn btn-dark DarkModeToggler" @click="darkMode">
    <i class="fa fa-moon" /> dark
  </button>
  <div :[attribute]="classes">
    <h1 :[attribute]="themeD">DC Heroes</h1>
    <span class="p-0"
      ><img
        src="https://th.bing.com/th/id/OIP.DL-XesiiZEfcnyn3D4fvVQHaHa?w=200&h=200&c=0&r=0&o=0&pid=0"
        alt=""
      />
    </span>

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
      themeD: "text-black",
      attribute: "class",
      classes: "vh-100 w-100 m-0 d-flex flex-column align-items-center",
    };
  },
  methods: {
    darkMode() {
      this.classes == "vh-100 w-100 m-0 d-flex flex-column align-items-center"
        ? ((this.classes =
            "vh-100 m-0 w-100 bg-dark d-flex flex-column align-items-center"),
          (this.themeD = "text-white"))
        : ((this.classes =
            "vh-100 w-100 m-0 d-flex flex-column align-items-center"),
          (this.themeD = "text-black"));
      // if(this.classes=="vh-100 w-100 m-0 d-flex flex-column align-items-center"){
      //   this.classes="vh-100 m-0 w-100 bg-dark d-flex flex-column align-items-center";
      //   this.themeD ='text-white';
      // }
      // else{
      //   this.classes="vh-100 w-100 m-0 d-flex flex-column align-items-center";
      //   this.themeD ='text-black';
      // }
    },
  },
  components: {
    Nav,
  },
};
</script>

<style>
.DarkModeToggler {
  position: absolute;
  top: 20px;
  right: 20px;
}

h1 {
  margin-top: 60px;
  font-size: 50px;
}
img {
  border-radius: 50%;
}
</style>
