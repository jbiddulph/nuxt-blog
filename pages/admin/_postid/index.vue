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
  layout: 'admin',
  components: {
    AdminPostForm
  },
  data () {
    return {
      loadedPost: {
        author: 'John Biddulph',
        title: 'This is a title',
        content: 'Super amazing thanks!',
        thumbnailLink: 'https://www.positive.news/wp-content/uploads/2019/03/feat-1800x0-c-center.jpg'
      }
    }
  }
}
</script>

<style scoped>
.update-form {
  width: 90%;
  margin: 20px auto;
}
@media (min-width: 768px) {
  .update-form {
    width: 500px;
  }
}
</style>
