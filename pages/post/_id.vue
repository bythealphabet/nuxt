<template>
  <div>
    <h1>
      {{ comment.name }}
    </h1>
    <p>
      {{ comment.body }}
    </p>
    <img :src="comment.img" alt="comment.name" />
  </div>
</template>

<script>
import comments from "~/data/comments.json";

export default {
  data() {
    return {
      comment: {},
    };
  },
  created() {
    const comment = comments.find((post) => {
      const paramID = Number(this.$route.params.id);
      const postID = Number(post.id);

      return postID === paramID;
    });
    this.comment = comment;
  },
};
</script>
