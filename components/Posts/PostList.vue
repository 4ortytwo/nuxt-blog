<template>
  <section class="post-list">
    <PostPreview
      id="1"
      :is-admin="isAdmin"
      :thumbnail="menImg"
      title="Hello there!"
      previewText="This is my first post"
    />
    <PostPreview
      id="2"
      :is-admin="isAdmin"
      :thumbnail="downloadImg"
      title="Hello there the Second time!"
      previewText="This is my second post"
    />
    <PostPreview
      id="3"
      :is-admin="isAdmin"
      thumbnail="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQwQeUDWcs60whCTdBsBm1IN1LL0w8ObwwPod55I2siEGWnXNT5FA&s"
      title="Hi, this is my third post!"
      previewText="This is my third post"
    />
  </section>
</template>

<script>
import PostPreview from '@/components/Posts/PostPreview'
export default {
  components: {
    PostPreview
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false,
    }
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
.post-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
