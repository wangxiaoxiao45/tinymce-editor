<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <div class="text-container">
      <TinymceEditor v-model="txtString"></TinymceEditor>
    </div>
  </div>
</template>

<script>
import TinymceEditor from './components/TinymceEditor.vue'

export default {
  name: 'App',
  components: {
    TinymceEditor,
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
  width: 700px;
}
</style>
