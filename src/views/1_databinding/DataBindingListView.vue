<template>
  <div>
    <div>
      <select name="" id="">
        <option value=""></option>
        <option :value="city.code" v-for="city in cities" :key="city.code">
          {{ city.title }}
        </option>
      </select>
    </div>
    <div>
      <table>
        <thead>
          <tr>
            <th>제품번호</th>
            <th>제품명</th>
            <th>가격</th>
            <th>주문수량</th>
            <th>합계</th>
          </tr>
        </thead>
        <tbody>
          <tr :key="drink.drinkId" v-for="drink in drinkList">
            <td>{{ drink.drinkId }}</td>
            <td>{{ drink.drinkName }}</td>
            <td>{{ drink.price }}</td>
            <td><input type="number" v-model="drink.qty" /></td>
            <td>{{ drink.price * drink.qty }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      cities: [
        { title: "서울", code: "02" },
        { title: "부산", code: "051" },
        { title: "제주", code: "064" },
      ],
      drinkList: [
        {
          drinkId: "1",
          drinkName: "코카콜라",
          price: 90000,
          qty: 1,
        },
        {
          drinkId: "2",
          drinkName: "포도주스",
          price: 80000,
          qty: 1,
        },
        {
          drinkId: "3",
          drinkName: "오렌지주스",
          price: 90000,
          qty: 1,
        },
      ],
    };
  },
});
</script>
