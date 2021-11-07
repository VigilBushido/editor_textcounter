<template>
  <div>
    <input v-model="message" />
    <button @click="$emit('send', message)">Emit inline</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: null,
    };
  },
  methods: {
    send() {
      this.$emit("send", this.message);
    },
  },
};
</script>

<style></style>
