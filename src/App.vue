<template>
  <div id="app">
    <EventsTest
      :click-event="{name: 'ClickEvent', action:clickMe}"
      :table-headers="['Name', 'Number', 'Registered']"
      :table-data="[
        ['James', '392840', 'Y'],
        ['Jen', '39048', 'N']
      ]"/>
  </div>
</template>

<script>
import EventsTest from './components/EventsTest.vue'

export default {
  name: 'app',
  components: {
    EventsTest
  },
  methods: {
    clickMe() {
      console.log('You clicked me')
    },
    dismiss() {
      console.log('You dismissed me')
    }
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
