<template>
  <div v-for="component in components" :key="component.name">
    <component :is="{...component}"/>
  </div>
</template>

<script>
import bazaar from './components'

export default {
  name: 'App',

  data() {
      return {
          components: null
      }
  },

  mounted() {
    this.components = bazaar
  }
}
</script>

<style lang="scss">
  @import "./App.scss";

  body {
    margin: 0;
    padding: 0;
  }
</style>
