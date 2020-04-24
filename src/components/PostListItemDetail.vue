<template>
  <b-card tag="article" class="mb-2">
    <div v-if="post.title">
      <h3>{{ post.title }}</h3>
      <b-card-text>{{ post.body }}</b-card-text>
    </div>
    <div class="text-center" v-else>
      <b-spinner variant="success" label="Loading"></b-spinner>
    </div>
  </b-card>
</template>

<script>
export default {
  name: 'PostListItemDetail',
  props: ['post']
};
</script>