<template>
    <div class="content">
        <slot></slot>
    </div>
</template>

<script>
    export default {
        name: "sad-layout-content"
    }
</script>

<style lang="scss" scoped>
    .content {
        flex: 1;
        flex-grow: 1;
    }
</style>
>