<!-- src/components/Hello.vue -->

<template>
    <div>
        <div class="greeting">Hello {{ number }}</div>
        <slot name="top"></slot>
        <slot name="bottom"></slot>
        <div>Progress {{ test }} </div>
    </div>
</template>

<script lang="ts">
    import Vue from "vue";

    export default Vue.extend({
        data() {
            return {
                number: 6
            }
        },
        props: ['test']
    });
</script>

<style>
    .greeting {
        font-size: 20px;
    }
</style>