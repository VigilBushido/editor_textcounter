<template>
  <div id="app">
    <EditorWordCounter />
    <p>Mssage: {{ message }}</p>
    <MessageEditor @send="message = $event" />
    <button @click="message = null">Reset</button>
    <!--Activity 4.01-->
    <MessageFeed :messages="messages" />
    <LocalMessageEdit @send="onSend($event)" />
  </div>
</template>

<script>
import EditorWordCounter from "./components/EditorWordCounter";
import MessageEditor from "./components/MessageEditor";
import LocalMessageEdit from ".components/LocalMessageEdit";
import MessageFeed from ".components/MessageFeed";

export default {
  name: "App",
  components: {
    EditorWordCounter,
    MessageEditor,
    LocalMessageEdit,
    MessageFeed,
  },
  data() {
    return {
      message: null,
    };
  },
  methods: {
    onSend(event) {
      this.messages = [...this.messages, event];
    },
  },
};
</script>

<style lang="scss"></style>
