<template>
  <h3>Todo List</h3>
  <ul>
    <todo-item 
    v-for="x in items"
    :key="x"
    :item-name="x"
    style="background-color: lightgreen;"
    />
  </ul>
  <input v-model="newItem">
  <button @click="addItem">Add</button>
  <button @click="removeItem">Remove</button>
  

  
  
</template>

<script>
export default{
  methods : {
    addItem(){
      this.items.push(this.newItem);
      this.newItem = '';
    },
    removeItem(){
      this.items.pop(this.newItem);
      this.newItem = '';
    }
  },

  data(){

    return{
      newItem: '',
      items: ['Buy apples','Make pizza','Mow the lawn']
        
        };
      
    }
  }






</script>

<style>
#wrapper {
    display: flex;
    flex-wrap: wrap;
  }
  #wrapper > div {
    border: dashed black 1px;
    margin: 10px;
    padding: 0 20px;
    background-color: lightgreen;
  }



</style>
