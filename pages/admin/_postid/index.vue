<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost" />
    </section>
  </div>
</template>

<script>
import AdminPostForm from '@/components/Admin/AdminPostForm'
export default {
  components: {
    AdminPostForm
  },
  data() {
    return {
      menImg: require('@/assets/images/men.jpg'),
      loadedPost: {
        author: "Arthur Burgan",
        title: "My Magnificent Post",
        content: "Great text of unrivalled complexity",
        thumbnailLink: this.menImg
      }
    }
  }
}
</script>

<style scoped>

</style>
