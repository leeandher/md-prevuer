<template>
  <div class="preview-pane pane">
    <div class="preview-content" v-html="html" :style="css"/>
  </div>
</template>

<script>
export default {
  name: "PreviewPane",
  props: {
    html: String,
    css: String
  }
};
</script>

<style scoped>
.preview-pane {
  padding: 1.5rem;
}
.preview-content {
  font-size: 15px;
}
</style>

