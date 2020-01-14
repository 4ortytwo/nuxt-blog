<template>
  <div class="posts-page">
    <PostList />
  </div>
</template>

<script>
import PostList from '@/components/Posts/PostList'
export default {
  components: {
    PostList
  },
  data() {
    return {
      menImg: require('@/assets/images/men.jpg'),
      downloadImg: require('@/assets/images/downloadImg.jpeg')
    }
  }

}
</script>

<style scoped>
.posts-page {
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
