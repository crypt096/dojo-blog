<template>
  <div class="home">home</div>
  <h1>Home</h1>
  <PostList :posts="posts" />
</template>

<script>
import PostList from "../components/PostList";
import { ref } from "vue";
export default {
  name: "Home",
  components: {
    PostList,
  },
  setup() {
    const posts = ref([
      {
        title: "welcome to the blog",
        body:
          "Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus ipsam enim, reprehenderit facere est eligendi earum voluptatibus fugit debitis! Est, incidunt quo in fugiat doloremque sit quae repellat illo veritatis nam dolor. Eveniet culpa eius fuga iusto nostrum libero obcaecati ex excepturi facere molestias. Aliquam ab exercitationem iste voluptates explicabo quae eos autem et quas fugiat itaque, veniam in qui officiis? Deserunt facere optio iste consequatur necessitatibus",
        id: 1,
      },
      { title: "top 5 css tips", body: "lorem ipsum", id: 2 },
    ]);
    return { posts };
  },
};
</script>