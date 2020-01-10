<template>
  <div class="posts-page">
    <section class="posts-list">
      <PostPreview
        id="1"
        :thumbnail="menImg"
        title="Hello there!"
        previewText="This is my first post"
      />
      <PostPreview
        id="2"
        :thumbnail="downloadImg"
        title="Hello there the Second time!"
        previewText="This is my second post"
      />
      <PostPreview
        id="3"
        thumbnail="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQwQeUDWcs60whCTdBsBm1IN1LL0w8ObwwPod55I2siEGWnXNT5FA&s"
        title="Hi, this is my third post!"
        previewText="This is my third post"
      />
    </section>
  </div>
</template>

<script>
import PostPreview from '@/components/Posts/PostPreview'
export default {
  components: {
    PostPreview
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

.posts-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
