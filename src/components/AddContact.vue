<template>
<div class="host">
  <paper-input label="Add a contact" no-label-float v-bind:value="contact" v-on:input="contact = $event.target.value" @keyup.enter="submit"></paper-input>
</div>
</template>

<script>
export default {
  data () {
    return {
      contact: ''
    }
  },
  methods: {
    submit: function () {
      if (this.contact) {
        this.$emit('submit', this.contact)
        this.contact = ''
      }
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.host {
  padding: 10px;
}
</style>
