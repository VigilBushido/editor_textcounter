<template>
  <div id="app">
    <EditorWordCounter />
    <MessageEditor />
  </div>
</template>

<script>
import EditorWordCounter from "./components/EditorWordCounter";
import MessageEditor from "./components/MessageEditor";

export default {
  name: "App",
  components: {
    EditorWordCounter,
    MessageEditor,
  },
};
</script>

<style lang="scss"></style>
