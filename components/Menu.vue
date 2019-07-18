<template>
  <div>
    <a-menu
      :default-selected-keys="['1']"
      :open-keys.sync="openKeys"
      mode="inline"
      @click="handleClick"
    >
      <a-sub-menu key="sub1" @titleClick="titleClick">
        <span slot="title">
          <a-icon type="folder" />
          <span>銷售管理</span>
        </span>
        <a-menu-item key="1">
          訂單查詢
        </a-menu-item>
        <a-menu-item key="2">
          訂單明細
        </a-menu-item>
        <a-sub-menu key="sub2" title="訂單處理">
          <a-menu-item key="3">
            變更訂單狀態
          </a-menu-item>
          <a-menu-item key="4">
            付款狀態
          </a-menu-item>
          <a-menu-item key="5">
            配送狀態
          </a-menu-item>
          <a-menu-item key="6">
            接單狀態
          </a-menu-item>
        </a-sub-menu>
      </a-sub-menu>
      <a-sub-menu key="sub3" @titleClick="titleClick">
        <span slot="title">
          <a-icon type="appstore" />
          <span>商品管理</span>
        </span>
        <a-menu-item key="7">
          品牌管理
        </a-menu-item>
        <a-menu-item key="8">
          商品類別管理
        </a-menu-item>
        <a-sub-menu key="sub4" title="商品管理">
          <a-menu-item key="9">
            商品編修
          </a-menu-item>
          <a-menu-item key="10">
            商品一覽表
          </a-menu-item>
          <a-menu-item key="11">
            關連商品設定
          </a-menu-item>
          <a-menu-item key="12">
            推薦商品設定
          </a-menu-item>
          <a-menu-item key="13">
            熱門商品設定
          </a-menu-item>
          <a-menu-item key="14">
            新品上市設定
          </a-menu-item>
        </a-sub-menu>
      </a-sub-menu>
      <a-sub-menu key="sub5">
        <span slot="title">
          <a-icon type="shop" />
          <span>行銷管理</span>
        </span>
        <a-menu-item key="15">
          商品設定
        </a-menu-item>
        <a-menu-item key="16">
          單價設定
        </a-menu-item>
        <a-menu-item key="17">
          活動設定
        </a-menu-item>
        <a-menu-item key="18">
          優惠卷設定
        </a-menu-item>
        <a-menu-item key="19">
          加購設定
        </a-menu-item>
      </a-sub-menu>
      <a-sub-menu key="sub6">
        <span slot="title">
          <a-icon type="cloud" />
          <span>線上資訊管理</span>
        </span>
        <a-menu-item key="20">
          廣告輪播
        </a-menu-item>
        <a-menu-item key="21">
          最新消息
        </a-menu-item>
        <a-menu-item key="22">
          獨享說明
        </a-menu-item>
        <a-menu-item key="23">
          熱門連結
        </a-menu-item>
        <a-menu-item key="24">
          關聯網站
        </a-menu-item>
      </a-sub-menu>
      <a-sub-menu key="sub7">
        <span slot="title">
          <a-icon type="dollar" />
          <span>帳務管理</span>
        </span>
        <a-menu-item key="25">
          帳務統計表
        </a-menu-item>
        <a-menu-item key="26">
          帳務明細表
        </a-menu-item>
      </a-sub-menu>
      <a-sub-menu key="sub8">
        <span slot="title">
          <a-icon type="mail" />
          <span>電子報</span>
        </span>
        <a-menu-item key="27">
          媒合寄送
        </a-menu-item>
        <a-menu-item key="28">
          批量寄送
        </a-menu-item>
        <a-menu-item key="29">
          電子報樣板設定
        </a-menu-item>
        <a-menu-item key="30">
          訂閱名單管理
        </a-menu-item>
      </a-sub-menu>
      <a-sub-menu key="sub9">
        <span slot="title">
          <a-icon type="setting" />
          <span>系統管理</span>
        </span>
        <a-menu-item key="31">
          後台帳號管理
        </a-menu-item>
        <a-menu-item key="32">
          配送方式設定
        </a-menu-item>
        <a-menu-item key="33">
          付款方式設定
        </a-menu-item>
        <a-menu-item key="34">
          訊息模板設定(簡信/Email)
        </a-menu-item>
        <a-menu-item key="35">
          會員系統連接
        </a-menu-item>
      </a-sub-menu>
    </a-menu>
  </div>
</template>
<script>
export default {
  data() {
    return {
      current: ['mail'],
      openKeys: ['sub1']
    }
  },
  watch: {
    openKeys(val) {
      // console.log('openKeys', val)
    }
  },
  methods: {
    handleClick(e) {
      // console.log('click', e)
    },
    titleClick(e) {
      // console.log('titleClick', e)
    }
  }
}
</script>

<style>
/* .ant-menu-vertical .ant-menu-item,
.ant-menu-vertical-left .ant-menu-item,
.ant-menu-vertical-right .ant-menu-item,
.ant-menu-inline .ant-menu-item, */
.ant-menu-vertical .ant-menu-submenu-title,
.ant-menu-vertical-left .ant-menu-submenu-title,
.ant-menu-vertical-right .ant-menu-submenu-title,
.ant-menu-inline .ant-menu-submenu-title {
  margin-top: 0;
}
</style>
