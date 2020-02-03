<template>
  <div class="home-page">
    <section class="intro">
      <h1>Work together!</h1>
    </section>
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
import PostList from '../components/Posts/PostList'
import menImg from '@/assets/images/men.jpg'

export default {
  components: {
    PostList
  },
  asyncData(context, callback) {
    setTimeout(() => {
      callback(null, {
        loadedPosts: [
          {
            id: '1',
            title: 'First Post',
            previewText: 'My first post',
            thumbnail: menImg
          },
          {
            id: '2',
            title: 'Second Post',
            previewText: 'My second post',
            thumbnail: menImg
          },
          {
            id: '3',
            title: 'Third Post',
            previewText: 'My third post',
            thumbnail: menImg
          }
        ]
      })
    }, 1500)
  }
  // data() {
  //   return {
  //     loadedPosts: []
  //   }
  // },
  // created() {
  //   setTimeout(() => {
  //     this.loadedPosts = [
  //       {
  //         id: '1',
  //         title: 'First Post',
  //         previewText: 'My first post',
  //         thumbnail: menImg
  //       },
  //       {
  //         id: '2',
  //         title: 'Second Post',
  //         previewText: 'My second post',
  //         thumbnail: menImg
  //       },
  //       {
  //         id: '3',
  //         title: 'Third Post',
  //         previewText: 'My third post',
  //         thumbnail: menImg
  //       }
  //     ]
  //   }, 1500)
  // }
}
</script>

<style scoped>
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url('~assets/images/JcuPgit-cyberpunk-wallpaper.jpg');
  background-position: center;
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}
</style>
