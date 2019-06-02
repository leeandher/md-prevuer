<template>
  <div class="edit-pane">
    <div class="edit-content" v-html="html" :style="css"/>
  </div>
</template>

<script>
export default {
  name: "EditPane"
};
</script>

<style scoped>
.edit-pane {
  max-width: 640px;
  margin: 2rem;
  border: 2px solid red;
}
</style>

