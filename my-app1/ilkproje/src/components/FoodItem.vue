
<template>
    <div>
      <h2>{{ foodName }}
    <img src="/55364608-meat-kebab.jpg" v-show="isFavorite"> 
    
    </h2>
    <p>{{ foodDesc }}</p>
    <button v-on:click="toggleFavorite">Favorite</button>
    
      
      
      
      
      
    </div>
  </template>
  
  <script>
  export default {
    
    

  props:['foodName','foodDesc','isFavorite'],
  emits:['toggleFavorite'],
  data(){
    return{
       // foodIsFavorite: this.isFavorite
    }
  },
  methods: {
    
    toggleFavorite(){
       // this.foodIsFavorite =!this.foodIsFavorite
        this.$emit('toggle-favorite',this.foodName);

    }
    
  }
       
       
    }
    
       
    
    
    

  
  </script>
  
  <style>
img{
    height: 100px;
    float: right;
}

</style>