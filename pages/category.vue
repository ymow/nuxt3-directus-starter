<template>
  <Category />
  <p v-if="categories[0]">{{categories[0].articles[0].title}}</p>
</template>
<script lang="ts">
import { defineComponent, onMounted, ref } from "vue";
import Category from "/components/Category.vue";
import axios from "axios";

export default defineComponent({
  setup() {
    const users = ref([]);
    const categories = ref([]);
    onMounted(async () => {
      const res = await axios.get("https://jsonplaceholder.typicode.com/users");
      users.value = res.data;
      console.log(res);
      const { $directus } = useNuxtApp()
      const response = await $directus.items('news_categories').readByQuery({
        fields: ["*", "articles.id", "articles.title", "articles.author.avatar", "articles.author.last_name"],
        filter: {
          status: { _eq: 'published' },
        },
        limit: 5,
      })
      categories.value = response.data
      console.log(categories);
    });

    return {
      users,
      categories,
    };
  },
  components: {
    Category,
  },
});
</script>
