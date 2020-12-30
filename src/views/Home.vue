<template>
  <div class="home">home</div>
  <p>My name is {{ name }} and my age is : {{ age }}</p>
  <button @click="handleClick">Click me</button>
  <button @click="age++">Increase age</button>
  <input type="text" v-model="name" />
</template>

<script>
import { ref } from "vue";
export default {
  name: "Home",
  setup() {
    const name = ref("Alex");
    const age = ref(24);

    // const p = ref(null);

    const handleClick = () => {
      name.value = "Luigi";
      age.value = 100;
    };

    return {
      name,
      age,
      handleClick,
    };
  },
  data() {
    return {
      score: 5,
    };
  },
};
</script>
