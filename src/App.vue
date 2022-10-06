<template>
  <div class="c-app">
    <top-navbar />
    <div v-for="component in components" :key="component.name">
      <component :is="{...component}"/>
    </div>
  </div>
</template>

<script>
import TopNavbar from './components/utils/TopNavbar.vue'
import bazaar from './components'

export default {
  components: { TopNavbar },
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
