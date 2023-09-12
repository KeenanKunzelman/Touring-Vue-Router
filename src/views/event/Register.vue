<template>
  <p>Register for the event here</p>
  <button @click="register">Register Me</button>
</template>

<script>
export default {
  props: ['event'],
  inject: ['Gstore'],
  methods: {
    register() {
      // Call to API
      // If registered then redirect to event details
      this.Gstore.flashMessage = 
        'You are successfully registered for ' + this.event.title
      setTimeout(() => {
        this.Gstore.flashMessage = ''
      }, 3000);
      this.$router.push({
        name: 'EventDetails'
      })
    }
  }
}
</script>
