<template>
    <div>
        <div><h2>制造执行系统</h2></div>

        <a-menu v-model="current" mode="horizontal">

            <a-menu-item key="mail"> 我的面板</a-menu-item>
            <a-menu-item key="app" disabled> 系统设置</a-menu-item>
            <a-menu-item key="" disabled> 基础资料管理</a-menu-item>
            <a-menu-item key="" disabled> 工艺管理 </a-menu-item>
            <a-menu-item key="app" disabled> 生产管理 </a-menu-item>
            <a-menu-item key="app" disabled> 质量管理</a-menu-item>
            <a-menu-item key="app" disabled> 绩效管理</a-menu-item>
            <a-menu-item key="app" disabled> 设备管理</a-menu-item>

        </a-menu>
    </div>
</template>
<script>
    export default {
        name:"sys-header",
        data() {
            return {
                current: ['mail'],
            };
        },
    };
</script>
<style>
div>h2{
    float: left;
    margin-right: 20px;
}
</style>
