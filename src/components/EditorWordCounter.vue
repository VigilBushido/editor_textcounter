<template>
  <div>
    <ul v-if="count">
      <li>Paragraphs: {{ count.paragraphs }}</li>
      <li>Sentences: {{ count.sentences }}</li>
      <li>Words: {{ count.words }}</li>
    </ul>
    <textarea ref="textArea" cols="50" rows="7"> </textarea>
  </div>
</template>

<script>
import * as Countable from "countable";
export default {
  mounted() {
    Countable.on(this.$refs.textArea, (count) => {
      this.count = count;
    });
    // we need to remove the Countable event listener when the component is destroyed() {
    this.$once("hook:beforeDestroy", function () {
      Countable.off(this.$refs.textArea);
    });
  },
  data() {
    return {
      count: null,
    };
  },
};
</script>

<style></style>
