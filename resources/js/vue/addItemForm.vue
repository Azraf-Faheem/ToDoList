<template>
    <div class="addItem">
      <input type="text" v-model="newItem" @keyup.enter="addItem" placeholder="Add a new item">
      <button @click="addItem">Add</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        newItem: "", // Store the input value here
      };
    },
    methods: {
      addItem() {
        // Emit an event to notify the parent component about the new item
        this.$emit("add-item", this.newItem);
        // Clear the input field after adding the item
        this.newItem = "";
      },
    },
  };
  </script>
  
  <style scoped>
  /* Scoped styles for the AddItemForm component */
  .addItem {
    margin: 20px 0;
    display: flex;
    align-items: center;
  }
  
  input[type="text"] {
    flex: 1;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 16px;
  }
  
  button {
    margin-left: 10px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 4px;
    padding: 10px 20px;
    cursor: pointer;
    font-size: 16px;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  </style>
  