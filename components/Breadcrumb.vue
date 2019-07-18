<template>
  <a-breadcrumb class="container">
    <a-breadcrumb-item>首頁</a-breadcrumb-item>
    <a-breadcrumb-item v-for="item in breadList" :key="item.name">
      {{ item.name }}
    </a-breadcrumb-item>
  </a-breadcrumb>
</template>

<script>
export default {
  data() {
    return {
      breadList: [],
      name: ''
    }
  },
  watch: {
    $route() {
      this.getBreadcrub()
    }
  },
  created() {
    this.getBreadcrub()
  },
  methods: {
    getBreadcrub() {
      console.log('start')
      this.breadList = []
      this.name = this.$route.name
      this.$route.matched.forEach((item) => {
        this.breadList.push(item)
      })
      console.log(this.breadList)
    }
  }
}
</script>

<style scoped>
.container {
  padding: 16px;
}
</style>
