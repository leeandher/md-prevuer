<template>
  <div id="app">
    <div id="content-panel">
      <EditPane @edit="handleEdit"/>
      <PreviewPane :html="rawHtml" css/>
    </div>
    <div id="function-panel"></div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import PreviewPane from "./components/PreviewPane.vue";
import EditPane from "./components/EditPane.vue";
import FunctionButton from "./components/FunctionButton.vue";

export default {
  name: "app",
  components: {
    PreviewPane,
    EditPane,
    FunctionButton
  },
  data() {
    return {
      rawHtml: EditPane.data().rawInput
    };
  },
  methods: {
    handleEdit(newValue) {
      console.log(newValue);
      this.rawHtml = newValue;
    }
  }
};
</script>

<style>
:root {
  --light: #f7f7f7;
  --dark: #22303d;
}
html {
  font-size: 10px;
}
body {
  margin: 0;
  padding: 0;
  position: relative;
  background: var(--light);
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--dark);
}
#content-panel {
  display: flex;
  margin: 2rem;
  flex-flow: row wrap;
}
.pane {
  border-radius: 0.5rem;
  border: 2px solid var(--dark);
  box-shadow: var(--dark) 0 2px 3px;
  max-width: 640px;
  margin: 1rem;
  flex: 1;
  flex-basis: 275px;
}
</style>
