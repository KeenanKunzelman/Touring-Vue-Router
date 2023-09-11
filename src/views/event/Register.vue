<template>
  <p>Register for the event here</p>
  <button @click="register">Register Me</button>
</template>

<script>
export default {
  props: ['event'],
  methods: {
    register () {
      //call api 
      this.$router.push({
        name: 'EventDetails',
      })
    }
  }
}
</script>
