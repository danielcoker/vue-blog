<template>
  <PostList />
</template>

<script>
// @ is an alias to /src
import PostList from '@/components/PostList';

export default {
  name: 'Home',
  title: 'Home - My Blog',
  components: {
    PostList,
  },
};
</script>
