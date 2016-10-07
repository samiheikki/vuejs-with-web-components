<template>
<div id="app">
  <paper-material elevation="1" id="material">
    <heading></heading>
    <add-contact v-on:submit="addContact"></add-contact>
    <contact v-for="contact in contacts" :name="contact.name" :id="contact.id" v-on:remove="removeContact">
    </contact>
  </paper-material>
</div>
</template>

<script>
import Heading from './components/Heading'
import AddContact from './components/AddContact'
import Contact from './components/Contact'

export default {
  components: {
    Heading,
    AddContact,
    Contact
  },
  data () {
    return {
      contacts: [],
      id: 0
    }
  },
  methods: {
    addContact: function (name) {
      this.contacts.push({
        name: name,
        id: this.id
      })
      this.id++
    },
    removeContact: function (id) {
      this.contacts = this.contacts.filter(function (contact) {
        return contact.id !== id
      })
    }
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  width: 420px;
  display: block;
  position: relative;
  background: #fff;
}

#material {
  width: 100%;
  height: 100%;
  border-radius: 10px;
}
</style>
