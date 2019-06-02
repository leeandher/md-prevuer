<template>
  <div class="edit-pane pane">
    <textarea name="editor" v-model="rawInput" @keyup="$emit('edit', rawInput)" rows="30"/>
  </div>
</template>

<script>
export default {
  name: "EditPane",
  data: function() {
    return {
      rawInput: `# Marked

## This is actually fucking working

#### What the actual fuck

>That's awesome

\`code\`

thats wack and a half

**BOLD**


**ITALICS**
      
      `
    };
  }
};
</script>

<style scoped>
textarea {
  border: 0;
  background: transparent;
  outline: 0;
  resize: vertical;
  padding: 0.5rem;
  width: calc(100% - 1rem);
}
textarea::-webkit-scrollbar {
  width: 1rem;
  border-radius: 1.25rem;
}
textarea::-webkit-scrollbar-thumb {
  background: var(--dark);
}
</style>

