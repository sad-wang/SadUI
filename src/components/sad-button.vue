<template>
    <button :class="[`icon-${iconPosition}`]" class="sad-button">
        <sad-icon v-if="icon" :name="icon" class="icon"/>
        <div class="content">
            <slot/>
        </div>
    </button>
</template>

<script>
    import SadIcon from "./sad-icon";
    export default {
        name: "sad-button",
        components: {SadIcon},
        props:{
            icon: {},
            iconPosition: {
                type: String,
                default: 'left',
                validator (value) {
                    return value === 'left' || 'right'
                }
            }
        }
    }
</script>

<style  lang="scss" scoped>
    .sad-button{
        cursor: pointer;
        font-size: var(--font-size); height: var(--button-height); padding: 0 1em;
        border-radius: var(--border-radius); border: 1px solid var(--border-color);
        background: var(--button-bg);
        line-height: var(--button-height);
        display: inline-flex; justify-content: center; align-items: center;
        vertical-align: middle;
        &:hover { border-color: var(--border-color-hover); }
        &:active { background-color: var(--button-active-bg); }
        &:focus { outline: none; }
        > .content { order: 2; }
        > .sad-icon { order: 1; margin-right: .2em; }
        &.icon-right {
            > .content { order: 1; }
            > .icon { order: 2; margin-right: 0; margin-left: .2em;}
        }
        .loading {
            animation: spin 2s infinite linear;
        }
    }
    @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
    }
</style>