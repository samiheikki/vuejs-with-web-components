<template>
<div class="host">
  <div class="user">
    <img v-bind:src="img">
  </div>

  <div class="heading-user">
    <strong>{{name}}</strong>
    <br/>
    <small>@{{handler}}</small>
  </div>
</div>
</template>

<script>
export default {
  data () {
    return {
      name: 'Sami Suo-Heikki',
      handler: 'samisuoheikki',
      img: 'https://avatars2.githubusercontent.com/u/8615573?v=3&s=466'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.host {
  background-color: #3F51B5;
  color: #fff;
  padding: 20px;
  box-shadow: 0 2px 2px -2px #444;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}

h1 {
  color: #42b983;
}

.user {
  display: inline-block;
  float: left;
  margin-right: 15px;
  width: 10%;
}

.user img {
  width: 40px;
  border-radius: 50%;
  border: #fff 2px solid;
}
</style>
