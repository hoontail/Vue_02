<template>
  <div>Hello {{ userName }}</div>
  <p>{{ message }}</p>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      userName: "hoontail",
      message: "Welcome Vue",
      arr: [],
      obj: {},
    };
  },
});
</script>
