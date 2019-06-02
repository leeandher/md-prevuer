<template>
  <button @click="func">{{text}}</button>
</template>


<script>
export default {
  props: {
    text: String,
    func: Function
  }
};
</script>

<style scoped>
button {
  border: 2px solid red;
}
</style>

