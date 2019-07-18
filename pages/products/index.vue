<template>
  <a-table :columns="columns" :data-source="data" class="container" />
</template>
<script>
export default {
  data() {
    return {
      columns: [
        {
          title: '名稱',
          dataIndex: 'name',
          key: 'name'
        },
        {
          title: '顏色',
          dataIndex: 'color',
          key: 'color'
        },
        {
          title: '價格',
          dataIndex: 'price',
          key: 'price'
        }
      ],
      data: [
        { key: 1, name: 'phone', color: 'red', price: 20000 },
        { key: 2, name: 'camera', color: 'green', price: 30000 },
        { key: 3, name: 'ps4', color: 'blue', price: 10000 }
      ]
    }
  }
}
</script>

<style scoped>
.container {
  margin: 16px;
}
</style>
