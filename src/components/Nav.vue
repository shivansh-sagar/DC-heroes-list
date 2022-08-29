<!-- eslint-disable vue/multi-word-component-names -->
<template>
<div class=" card w-75">
  <ul class=" card-body">
    <span class=" card mb-3 "><input class=" card-body mb-3 input-group" v-model="newHero" placeholder="Type DC Hero Name Here"><button  type="submit" class="btn btn-primary"  @click="add(newHero)" >add</button></span>
    
    <li
      class="card card-body  d-flex flex-row align-items-center justify-content-between mb-1"
      v-for="(hero) in a"
      v-bind:key="hero.index"
    >
      <span>{{  hero.name }}</span>
    <span @click="del(hero,value)"><i  class='fa fa-x'></i></span>  
    </li>
  </ul>
  
</div>
</template>

<script>

export default {
    data() {
        return {
          
          newHero:'' ,
            a: [
                {name: 'superman'},
                {name: 'batman'},
                {name: 'aquaman'},
                {name: 'flash'},

            ],
        };
    },
    methods: {
        del(hero) {
            this.a.splice(this.a.indexOf(hero),1);
            //  this.a.push("shivansh");
            console.log(hero, this.a);
        },
        add() {
          if(this.newHero!=''){
            this.a.push({name: this.newHero});
            this.newHero = '';
           console.log(this.newHero);
        }
      }
    },
    components: {  }
};
</script>

<style>
  input{
    max-height: 20px;
    border:none;
    outline: none;
  }
</style>
