<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <div class="text-container">
      <vue-show-more-text
        :text="txtString"
        :lines="3"
        additional-container-css="margin:14px;"
        additional-content-css="font-size:16px;"
        additional-content-expanded-css="font-size:16px;"
        additional-anchor-css="font-size: 16px;"
        @click="change"
      />
    </div>
  </div>
</template>

<script>
import VueShowMoreText from './components/VueShowMoreText.vue'

export default {
  name: 'App',
  components: {
    VueShowMoreText,
  },
  data() {
    return {
      txtString: `Note: This property was originally implemented in WebKit and has some issues. It got standardized for legacy support. The CSS Overflow Module Level 3 specification also defines a line-clamp property, which is meant to replace this property and avoid its issues.`,
    }
  },
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
.text-container {
  width: 200px;
}
</style>
