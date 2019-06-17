<template>
    <button class="g-button">
        <slot></slot>
        <svg v-if="icon" class="icon">
            <use :xlink:href="`#i-${icon}`"></use>
        </svg>
    </button>
</template>
<script>
    export default {
        props:['icon','iconPosition']
    }
</script>
<style lang="sass">
    .g-button
        font-size: var(--font-size)
        height: var(--button-height)
        padding: 0 1em
        border-radius: var(--border-radius)
        border: 1px solid var(--border-color)
        background: var(--button-bg)

        .g-button:hover
            border-color: var(--border-color-hover)

        .g-button:active
            background-color: var(--button-active-bg)

        .g-button:focus
            outline: none

</style>