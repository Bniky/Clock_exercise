<template>
  <div id="app">
    <clock v-model="time" />
    <clock :value="s_time" @setSecondCurrentTime="s_time = $event" />
    
  </div>
</template>

<script>
import Clock from './components/Clock.vue'

export default {
  name: 'App',
  components: {
    Clock
  },
  data() {
    return {
      timer: '',
      counter: 0,
      time: {
        hours: "00",
        minutes: "00"
      },
      
      s_time: {
        hours: "00",
        minutes: "00"
      }
    }
  }   
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
