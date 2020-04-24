<template>
  <div>
    <TheHero />

    <b-container>
      <div v-if="posts.length">
        <b-row class="mt-5">
          <b-col md="4" v-bind:key="post.id" v-for="post in posts">
            <PostListItem v-bind:post="post" />
          </b-col>
        </b-row>
      </div>
      <div class="text-center" v-else>
        <b-spinner variant="success" label="Loading"></b-spinner>
      </div>
    </b-container>
  </div>
</template>

<script>
import TheHero from '@/components/TheHero';
import PostListItem from '@/components/PostListItem';
import axios from 'axios';

export default {
  name: 'PostList',
  components: {
    TheHero,
    PostListItem
  },
  data() {
    return {
      posts: []
    };
  },
  created() {
    axios
      .get('https://jsonplaceholder.typicode.com/posts?_limit=12')
      .then(response => {
        this.posts = response.data;
      })
      .catch(error => {
        console.log(error);
      });
  }
};
</script>
