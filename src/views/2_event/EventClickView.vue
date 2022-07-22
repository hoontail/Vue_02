<template>
  <button @click="increaseCounter">Add 1</button>
  <p>{{ counter }}</p>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    increaseCounter() {
      this.counter += 1;
    },
  },
});
</script>
