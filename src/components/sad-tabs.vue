<template>
    <div class="tabs">
        <slot></slot>
    </div>
</template>
<script>
    import Vue from 'vue'
    export default {
        name: "sad-tabs",
        props: {
            selected: {
                type: String,
                required: true
            }
        },
        data () {
            return {
                eventBus: new Vue()
            }
        },
        provide () {
            return {
                eventBus: this.eventBus
            }
        },
        mounted () {
            if (this.$children.length === 0) {
                console && console.warn &&
                console.warn('tabs的子组件应该是tabs-head和tabs-body，但你没有写子组件')
            }
            this.$children.forEach((vm) => {
                if (vm.$options.name === 'sad-tabs-head') {
                    vm.$children.forEach((childVm) => {
                        if (childVm.$options.name === 'sad-tabs-item'
                            && childVm.name === this.selected) {
                            this.eventBus.$emit('update:selected', this.selected, childVm)
                        }
                    })
                }
            })
        }
    }
</script>

<style scoped>

</style>