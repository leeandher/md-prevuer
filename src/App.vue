<template>
  <div id="app">
    <div id="content-panel">
      <PreviewPane html="<p>Hello</p><h1>WORLD</h1>" css/>
      <EditPane/>
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
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--dark);
  background: var(--light);
  height: 100vh;
}
#content-panel {
  display: flex;
  padding: 2rem;
  background: ;
}
</style>
