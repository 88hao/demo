<template>
    <div>

        <a-menu v-model="current" mode="horizontal"style="width: 1500px">

            <a-menu-item key="mail"> 企业列表</a-menu-item>
            <a-menu-item key="app" disabled> 企业添加</a-menu-item>


        </a-menu>
    </div>
</template>
<script>
    export default {
        name:"bas-card",
        data() {
            return {
                current: ['mail'],
            };
        },
    };
</script>
<style>

</style>
