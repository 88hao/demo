<template>
    <div id="bas-s">
        <a-menu mode="inline" :open-keys="openKeys" style="width: 256px" @openChange="onOpenChange">
            <a-sub-menu key="sub1">
                <span slot="title"><a-icon type="mail" /><span>设备资料管理</span></span>
                <a-menu-item key="1">
                    Option 1
                </a-menu-item>
                <a-menu-item key="2">
                    Option 2
                </a-menu-item>
                <a-menu-item key="3">
                    Option 3
                </a-menu-item>
                <a-menu-item key="4">
                    Option 4
                </a-menu-item>
            </a-sub-menu>
            <a-sub-menu key="sub2">
                <span slot="title"><a-icon type="appstore" /><span>资源基础资料</span></span>
                <a-menu-item key="5">
                    企业
                </a-menu-item>
                <a-menu-item key="6">
                    工厂
                </a-menu-item>
                <a-menu-item key="7">
                    车间
                </a-menu-item>
                <a-menu-item key="8">
                    产线
                </a-menu-item>
                <a-menu-item key="9">
                    工站
                </a-menu-item>
                <a-menu-item key="10">
                    工位
                </a-menu-item>
                <a-menu-item key="11">
                    员工
                </a-menu-item>
                <a-menu-item key="12">
                    工位与员工关系
                </a-menu-item>
                
            </a-sub-menu>
            <a-sub-menu key="sub4">
                <span slot="title"><a-icon type="setting" /><span>BOM资料管理</span></span>

            </a-sub-menu>
        </a-menu>
    </div>
</template>
<script>
    export default {
        name:"bas-side",
        data() {
            return {
                rootSubmenuKeys: ['sub1', 'sub2', 'sub4'],
                openKeys: ['sub1'],
            };
        },
        methods: {
            onOpenChange(openKeys) {
                const latestOpenKey = openKeys.find(key => this.openKeys.indexOf(key) === -1);
                if (this.rootSubmenuKeys.indexOf(latestOpenKey) === -1) {
                    this.openKeys = openKeys;
                } else {
                    this.openKeys = latestOpenKey ? [latestOpenKey] : [];
                }
            },
        },
    };
</script>
<style>

</style>
