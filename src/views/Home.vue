<template>
  <div class="home">home</div>
  <p ref="p">My name is {{ name }} and my age is : {{ age }}</p>
  <button @click="handleClick">Click me</button>
</template>

<script>
import { ref } from "vue";
export default {
  name: "Home",
  setup() {
    console.log(this);
    let name = "Alex";
    let age = 24;

    const p = ref(null);

    const handleClick = () => {
      console.log(p, p.value);
      p.value.classList.add("test");
      p.value.textContent = "hello,ninjas";
    };

    return {
      name,
      age,
      handleClick,
      p,
    };
  },
};
</script>
