<template>
  <div class="d-flex justify-content-center">
    <ul class="list-group mt-5 w-75">
      <li class="list-group-item list-group-item-action d-flex justify-content-start" v-for="user in usersList" :key="user.id">
        <div class="d-flex w-100 flex-column">
          <h3 class="text-left">{{user.name}}</h3>
          <p>{{user.email}}</p>
        </div>
        <small class="text-danger delete" @click="deleteUser(user.id)">&#10005;</small>
      </li>
    </ul>
  </div>
</template>

<script>
  import {
    mapGetters,
    mapActions
  } from "vuex";

  export default {
    name: 'Users',
    methods: {
      ...mapActions(["fetchUsers", "deleteUser"])
    },
    computed: mapGetters(["usersList"]),
    created() {
      this.fetchUsers()
    }
  }
</script>

<style>
 .delete {
   font-size: 18px;
   cursor: pointer;
 }
</style>