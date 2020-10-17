<template>
  <h1>count: {{ countRef }}</h1>
  <p>
    <!-- <button @click="count++">count: {{ count }}</button> -->
    <button @click="increase">increase</button>
    <button @click="decrease">decrease</button>
  </p>
</template>

<script>
import { ref } from "vue";

function useCount() {
  let countRef = ref(0);
  const increase = () => {
    countRef.value++;
  };
  const decrease = () => {
    countRef.value--;
  };
  return {
    countRef,
    increase,
    decrease
  };
}

export default {
  setup() {
    // console.log("所有生命周期钩子函数之前调用");
    // console.log(this); // this -> undefined
    // let count = ref(0);
    // 在setup中，count是一个对象
    // 在实例代理中，count是一个count.value
    // console.log(count);
    // const increase = () => {
    //   count.value++;
    // };
    // return {
    //   count,
    //   increase
    // };

    return {
      ...useCount()
    };
  },
};
</script>
