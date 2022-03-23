<template>
  <div>
    <ul>
      <li v-for="comment in comments" :key="comment.id">
        <post :post="comment" />
      </li>
    </ul>
  </div>
</template>

<script>
import comments from "~/data/comments.json";

export default {
  data() {
    return {
      comments,
    };
  },
};
</script>
