<template>
<div class="d-flex align-items-center justify-content-center">
  <form class="w-75" @submit.prevent="onUserSubmit">
    <div class="form-group mb-1">
      <input type="text" class="form-control" placeholder="Enter name" v-model="name">
    </div>
    <div class="form-group mb-1">
      <input type="text" class="form-control" placeholder="Enter email" v-model="email">
    </div>
    <button type="submit" class="btn btn-block btn-primary">Add</button>
  </form>
</div>
</template>

<script>
import { mapActions } from "vuex";

export default {
  name: 'AddUser',
  data(){
      return {
        name: '',
        email: ''
      }
  },
  methods:{
    ...mapActions(["addUsers"]),
    onUserSubmit() {
        this.addUsers({
          name: this.name,
          email: this.email
        })
    }
  }
}
</script>