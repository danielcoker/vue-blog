<template>
  <b-card tag="article" style="max-width: 20rem;" class="mb-2">
    <h3>{{ post.title }}</h3>
    <b-card-text>{{ post.body.slice(0, 100) }}</b-card-text>
    <b-button :to="{ name: 'PostDetail', params: { id: post.id } }" variant="success">View Post</b-button>
  </b-card>
</template>

<script>
export default {
  name: 'PostListItem',
  props: ['post']
};
</script>