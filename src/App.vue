<template>
  <div id="app">
    <EditorWordCounter />
    <p>Mssage: {{ message }}</p>
    <MessageEditor @send="message = $event" />
    <button @click="message = null">Reset</button>
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
  data() {
    return {
      message: null,
    };
  },
};
</script>

<style lang="scss"></style>
