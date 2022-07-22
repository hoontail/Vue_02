<template>
  <div v-html="htmlString" />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      htmlString: '<p style="color:red;">이건 어쩔때 쓰는걸가 ??</p>',
    };
  },
});
</script>
