<template>
  <a-table :columns="columns" :data-source="products" />
</template>

<script>
export default {
  data() {
    return {
      columns: [
        {
          title: 'id',
          dataindex: 'id',
          key: 'id'
        },
        {
          title: '名稱',
          dataindex: 'name',
          key: 'name'
        },
        {
          title: '顏色',
          dataindex: 'color',
          key: 'color'
        },
        {
          title: '價格',
          dataindex: 'price',
          key: 'price'
        }
      ],
      products: [
        { id: 1, name: 'phone', color: 'red', price: 20000 },

        { id: 2, name: 'camera', color: 'green', price: 30000 },
        { id: 3, name: 'ps4', color: 'blue', price: 10000 }
      ]
    }
  }
}
</script>
