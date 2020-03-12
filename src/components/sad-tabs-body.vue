<template>
    <div class="tabs-body">
        <slot></slot>
    </div></template>
<script>
    export default {
        name: "sad-tabs-body",
        inject: ['eventBus'],
        created(){
        }
    }
</script>

<style scoped>

</style>