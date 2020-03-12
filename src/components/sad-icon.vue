<template>
    <svg class="sad-icon">
        <use :xlink:href="`#i-${name}`"></use>
    </svg>
</template>
<script>
    import './svg'
    export default {
        name: "sad-icon",
        props: ['name']
    }
</script>
<style lang="scss" scoped>
    .sad-icon {width: 1em; height: 1em; }
</style>