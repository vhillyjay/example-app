<template>
    <form @submit.prevent="submit">
      <label for="name">Name:</label>
      <input id="name" v-model="form.name" />
      <label for="address">Address:</label>
      <input id="address" v-model="form.address" />
      <button type="submit">Submit</button>
    </form>
  </template>
  
<script>
  import { reactive } from 'vue'
  import { Inertia } from '@inertiajs/inertia'
  
  export default {
    setup () {
      const form = reactive({
        name: null,
        address: null,
      })
  
      function submit() {
        Inertia.post('/customers', form)
      }
  
      return { form, submit }
    },
  }
</script>