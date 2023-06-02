<script setup lang="ts">
import {
  default as EditorJS,
  type ToolConstructable,
} from "@editorjs/editorjs";
import Header from "@editorjs/header";

new EditorJS({
  holder: "editor",
  tools: {
    header: {
      class: Header as unknown as ToolConstructable,
      shortcut: "CMD+SHIFT+H",
      config: {
        placeholder: "Enter a header",
        levels: [1, 2, 3, 4, 5, 6],
      },
    },
  },
});
</script>

<template>
  <div class="container">
    <h1>Welcome to Tauri!</h1>
    <div id="editor"></div>
  </div>
</template>

<style scoped>
#editor {
  border: 1px solid #000;
}
</style>
