<template>
  <!-- keyup.enter 이런식으로 이용가능 밑에는 정식 -->
  <div>
    <input
      type="text"
      name=""
      id=""
      @keyup="checkEnter($event)"
      v-model="searchTxt"
    />
    <button @click="doSearch">조회</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      searchTxt: "",
    };
  },
  methods: {
    doSearch() {
      console.log(this.searchTxt);
      this.searchTxt = "";
    },
    checkEnter(event: any) {
      if (event.key === "Enter") {
        this.doSearch();
        this.searchTxt = "";
      }
    },
  },
});
</script>
