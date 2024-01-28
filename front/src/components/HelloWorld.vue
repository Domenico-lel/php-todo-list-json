<script>

import axios from 'axios';

export default {
  data() {
    return {
      tasks: [],
    };
  },
  mounted() {
    axios.get('http://localhost/php-todo-list-json/back/')
      .then(response => {
        this.tasks = response.data;
      })
      .catch(error => {
        console.error('Errore durante la richiesta API:', error);
      });
  },
};
</script>

<template>
  <div>
    <h1>Todo List</h1>
    
  </div>
</template>

<style scoped>

</style>
