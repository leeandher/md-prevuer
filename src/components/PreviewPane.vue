<template>
  <div class="preview-pane pane">
    <div class="preview" v-html="html"/>
  </div>
</template>

<script>
export default {
  name: "PreviewPane",
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
}
</style>

