<template>
  <div>
    <p v-for="(m, i) in messages" :key="i">
      {{ m }}
    </p>
  </div>
</template>

<script>
import "core-js/es/array";

export default {
  props: {
    messages: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style></style>
