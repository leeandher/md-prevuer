<template>
  <div id="app">
    <div id="content-panel">
      <EditPane @edit="handleEdit"/>
      <PreviewPane :html="rawHtml"/>
    </div>
    <div id="function-panel"></div>
  </div>
</template>

<script>
import marked from "marked";

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
      rawHtml: marked(EditPane.data().rawInput)
    };
  },
  methods: {
    handleEdit(rawInput) {
      this.rawHtml = marked(rawInput);
    }
  }
};
</script>

<style>
:root {
  --light: rgb(248, 248, 248);
  --dark: rgb(34, 48, 62);
  --green: rgb(65, 184, 131);
  --honeydew: rgb(226, 245, 236);
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
  justify-content: center;
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
a {
  color: var(--green);
}
blockquote {
  margin: 0.5rem 1.5rem;
  line-height: 1;
  padding: 0.1rem 1rem;
  border-radius: 0.25rem;
  border-left: 5px solid var(--green);
  background: var(--honeydew);
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}
code {
  background: var(--honeydew);
  padding: 0 0.5rem;
  font-family: Consolas, "Lucida Console", Monaco, monospace;
}
pre {
  background: var(--dark);
  border-radius: 0.25rem;
  padding: 0.5rem;
}
pre code {
  background: transparent;
  color: var(--light);
}
hr {
  height: 0px;
  border: 1px solid var(--green);
}
</style>
