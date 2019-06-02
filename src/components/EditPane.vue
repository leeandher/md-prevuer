<template>
  <div class="edit-pane pane">
    <textarea id="editor" v-model="rawInput" @keyup="$emit('edit', rawInput)" rows="30"/>
    <FunctionButton text="Export Markdown"/>
  </div>
</template>

<script>
import { defaultText } from "../assets/constants";

import FunctionButton from "./FunctionButton";

export default {
  name: "EditPane",
  components: {
    FunctionButton
  },
  data: function() {
    return {
      rawInput: defaultText
    };
  }
};
</script>

<style scoped>
.edit-pane:after {
  content: "EDITOR";
}
#editor {
  border: 0;
  background: transparent;
  outline: 0;
  resize: vertical;
  padding: 0.5rem;
  width: calc(100% - 1rem);
  height: calc(100% - 1rem - 35px);
  margin-bottom: 35px;
  font-size: 1.5rem;
}
#editor::-webkit-scrollbar {
  width: 1rem;
  border-radius: 1.25rem;
}
#editor::-webkit-scrollbar-thumb {
  background: var(--dark);
}
</style>
