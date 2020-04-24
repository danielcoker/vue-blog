<template>
  <b-container>
    <div v-if="post">
      <b-row class="mt-5">
        <b-col lg="8" offset-md="2">
          <PostListItemDetail v-bind:post="post" />
        </b-col>
      </b-row>
    </div>
  </b-container>
</template>

<script>
import PostListItemDetail from '@/components/PostListItemDetail';
import axios from 'axios';

export default {
  name: 'PostDetail',
  components: {
    PostListItemDetail
  },
  data() {
    return {
      postID: this.$route.params.id,
      post: {}
    };
  },
  created() {
    axios
      .get(`https://jsonplaceholder.typicode.com/posts/${this.postID}`)
      .then(response => {
        this.post = response.data;
      })
      .catch(error => {
        console.log(error);
      });
  }
};
</script>