<template>

  <div id="app">
      {{switch1Value}}
    <toggle-switch group="a" :options="myOptions" @change="log($event.value)" v-model="switch1Value"/>
    <toggle-switch group="b" :options="myOptions1" @change="log($event.value)" v-model="switch2Value"/>
    {{switch2Value}}
  </div>
</template>

<script>
import ToggleSwitch from '../src/components/ToggleSwitch.vue'

export default {
  name: 'app',
  components: {
    ToggleSwitch
  },
  data() {
      return {
          switch1Value: 'unknown',
          switch2Value: 'unknown',
        myOptions: {
            items: {
                delay: .4,
                preSelected: 'unknown',
                disabled: false,
                labels: [
                { name: 'Off', color: 'white', backgroundColor: 'red' },
                { name: 'unknown', color: 'white', backgroundColor: 'grey' },
                { name: 'On', color: 'white', backgroundColor: 'green' }
                ]
            }
        },
        myOptions1: {
            items: {
                delay: .4,
                preSelected: 'unknown',
                disabled: false,
                labels: [
                { name: 'Off', color: 'white', backgroundColor: 'red' },
                { name: 'unknown', color: 'white', backgroundColor: 'grey' },
                { name: 'On', color: 'white', backgroundColor: 'green' }
                ]
            }
        }
    }
  },
  methods:{
      log(m){
          console.log(m)
      }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
