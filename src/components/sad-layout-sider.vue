<template>
    <div class="sider">
        <slot></slot>
    </div>
</template>

<script>
    export default {
        name: "sad-layout-sider",
        methods: {}
    }
</script>

<style lang="scss" scoped>
    .sider {
        position: relative;
    > button {
        position: absolute;
        top: 0;
        right: 0;
    }
    }
</style>