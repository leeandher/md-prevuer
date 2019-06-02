<template>
  <div class="preview-pane">
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
  max-width: 640px;
}
</style>

