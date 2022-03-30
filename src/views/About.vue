<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button @click="toCustomPage">Add Custome Page</button>
  </div>
</template>
<script>
export default {
  methods: {
    toCustomPage() {
      console.log('add route')
      this.$router.addRoutes([{path: '/custom', component: () => import('@/views/Custom.vue'), name: 'custom'}])
    }
  }
}
</script>
