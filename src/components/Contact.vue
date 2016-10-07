<template>
<div class="host">
  {{name}}
  <paper-icon-button icon="icons:delete" v-on:click="remove"></paper-icon-button>
</div>
</template>

<script>
export default {
  props: ['name', 'id'],
  methods: {
    remove: function () {
      console.log('remove')
      this.$emit('remove', this.id)
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
