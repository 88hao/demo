<template>
  <div id="components-layout-demo-basic">
    <a-layout>
        <sysheader></sysheader>
      <a-layout>
        <a-layout-sider >
          <baside></baside>
        </a-layout-sider>
        <a-layout-content>
          <a-input-search
                placeholder="input search text"
                enter-button="Search"
                size="large"
                @search="onSearch"
        />
          <bascard></bascard>
          <bascontext></bascontext>
          </a-layout-content>
      </a-layout>
      <a-layout-footer>Footer</a-layout-footer>
    </a-layout>
  </div>
</template>

<script>
// @ is an alias to /src
import sysheader from './common/sys-header.vue'
import baside from './bas/bas-side.vue'
import bascontext from './bas/bas-context.vue'
import  bascard from './bas/bas-card.vue'
export default {
  name: 'Home',
  components: {
    sysheader,
    baside,
    bascontext,
    bascard,
  }
}
</script>
<style>


  #components-layout-demo-basic {

  }
  #components-layout-demo-basic .ant-layout-header,
  #components-layout-demo-basic .ant-layout-footer {
    line-height: 1.5;
  }
  #components-layout-demo-basic .ant-layout-sider {
    background: none;
    margin-right: 80px;
    color: #fff;
    line-height: 120px;
  }
  #components-layout-demo-basic .ant-layout-content .bascontxte{
    min-height: 120px;
    line-height: 120px;
  }
  #components-layout-demo-basic .ant-layout-content .ant-input-search{
    margin-bottom: 10px;
    width: 300px;
  }
  #components-layout-demo-basic > .ant-layout {
    margin-bottom: 48px;
  }
  #components-layout-demo-basic > .ant-layout:last-child {
    margin: 0;
  }

</style>
