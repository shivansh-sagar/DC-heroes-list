<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <h1 class='card-body'>{{count}}</h1>
</template>

<script>


export default {
data() {
    return {
        count: 0,
    
        
    
    props: {
        count: {
            num: Number,
            
            
        }
    },
    }

},


    
}
</script>

<style>

</style>