<template>
  <a-layout id="components-layout-demo-custom-trigger">
    <a-layout-sider
      v-model="collapsed"
      :trigger="null"
      collapsible
      theme="light"
    >
      <div class="logo" />
      <menu-component />
    </a-layout-sider>
    <a-layout>
      <a-layout-header style="background: #fff; padding: 0;">
        <a-icon
          class="trigger"
          :type="collapsed ? 'menu-unfold' : 'menu-fold'"
          @click="() => (collapsed = !collapsed)"
        />
      </a-layout-header>
      <a-layout-content style="background: #fff;">
        <breadcrumb />
        <nuxt />
      </a-layout-content>
      <a-layout-footer>footer</a-layout-footer>
    </a-layout>
  </a-layout>
</template>

<script>
import Breadcrumb from '~/components/Breadcrumb.vue'
import MenuComponent from '~/components/Menu.vue'

export default {
  components: { Breadcrumb, MenuComponent },
  data() {
    return {
      collapsed: false
    }
  }
}
</script>

<style>
.trigger {
  font-size: 18px;
  line-height: 64px;
  padding: 0 24px;
  cursor: pointer;
  transition: color 0.3s;
}

.trigger:hover {
  color: #1890ff;
}

#components-layout-demo-custom-trigger .logo {
  height: 32px;
  background-color: grey;
  margin: 16px;
}
</style>
