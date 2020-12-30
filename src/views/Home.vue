<template>
  <div class="home">home</div>
  <p>My name is {{ name }} and my age is : {{ age }}</p>
  <button @click="handleClick">Click me</button>
</template>

<script>
export default {
  name: "Home",
  setup() {
    let name = "Alex";
    let age = 24;

    const handleClick = () => {
      console.log("You clicked me");
    };

    return {
      name,
      age,
      handleClick,
    };
  },
};
</script>
