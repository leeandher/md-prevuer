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
      rawInput: `     
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

---

**This is some bold text if you're trying to be \`strong\`**

_This is some italicized text if you wanna \`em\`phasize anything_

> A fancy quote would go here

Some \`basic inline code\` with more text

\`\`\`
if (moreCode) {
  //put it here
  //multiline
}
\`\`\`

[I'm an inline link, check me out!](https://www.leander.xyz)
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
  height: calc(100% - 1rem);
}
textarea::-webkit-scrollbar {
  width: 1rem;
  border-radius: 1.25rem;
}
textarea::-webkit-scrollbar-thumb {
  background: var(--dark);
}
</style>

