<template>
  <div class="home">home</div>
  <h1>Home</h1>
  <input type="text" v-model="search" />
  <p>Search term: {{ search }}</p>
  <div v-for="name in matchingNames" :key="name">
    {{ name }}
  </div>
</template>

<script>
import { computed, ref } from "vue";
export default {
  name: "Home",
  setup() {
    const search = ref("");
    const names = ref([
      "mario",
      "yoshi",
      "luigi",
      "toad",
      "bowser",
      "koopa",
      "peach",
    ]);

    const matchingNames = computed(() => {
      return names.value.filter((name) => name.includes(search.value));
    });

    console.log(matchingNames);

    return {
      names,
      search,
      matchingNames,
    };
  },
};
</script>
