<template>
  <AddUser />
  <Users />
</template>

<script>

import AddUser from './components/AddUser.vue'
import Users from './components/Users.vue'
export default {
  name: 'App',
  components: {
    AddUser,
    Users,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
