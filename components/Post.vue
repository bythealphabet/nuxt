<template>
  <div class="post">
    <h1>{{ post.name }}</h1>
    <p>{{ post.body }}</p>

    <p class="email">
      {{ post.email }}
      {{ post.img }}
    </p>
    <!-- <img :src="img" alt="post.name" /> -->
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Home Page Nuxt",
      meta: [
        {
          name: "description",
          content: "This is the home page of the Nuxt.js project",
          hid: "description",
        },
      ],
    };
  },
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
};
</script>
