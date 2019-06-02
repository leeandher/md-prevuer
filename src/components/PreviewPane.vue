<template>
  <div class="preview-pane pane">
    <div class="preview" v-html="html"/>
    <FunctionButton text="Export HTML"/>
  </div>
</template>

<script>
import FunctionButton from "./FunctionButton";

export default {
  name: "PreviewPane",
  components: {
    FunctionButton
  },
  props: {
    html: String
  }
};
</script>

<style scoped>
.preview-pane {
  padding: 1.5rem;
}
.preview-pane:after {
  content: "PREVIEW";
}
.preview {
  font-size: 15px;
  text-align: left;
  margin-bottom: 35px;
}
</style>

