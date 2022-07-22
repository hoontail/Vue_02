<template>
  <div :class="{ 'text-red': hasError, active: isActive }">클래스 바인딩</div>
  <div :class="class2">클래스바인딩2</div>
  <div :style="style1">스타일 바인딩</div>
  <button @click="style1.color = 'green'">스타일 변경</button>
</template>

<script lang="ts">
import { defineComponent } from "vue";
// 클래스바인딩 boolean 값으로 간편하게 css를 수정할 수 있다.
// 클래스2번은 쓸일 별로 없음
// style binding은 data에 오브젝트 형태로 이용하면됨(카멜케이스)
export default defineComponent({
  data() {
    return {
      isActive: false,
      hasError: false,
      class2: ["active", "text-red"],
      style1: { color: "blue", fontSize: "25px" },
    };
  },
});
</script>
<style scoped>
.active {
  background-color: greenyellow;
  font-weight: bold;
}
.text-red {
  color: red;
}
</style>
