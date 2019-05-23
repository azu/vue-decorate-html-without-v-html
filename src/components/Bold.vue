<template>
<!-- Vue does not support multiple template on root: https://github.com/vuejs/vue/issues/5758-->
<!-- Vue does not support Fragment: https://github.com/vuejs/vue/issues/7606-->
<!-- We want to write instead of it
    <template v-if='tagType === "strong"'>
        <strong>
            <slot>test</slot>
        </strong>
    </template>
    <template v-else>
        <b>
            <slot></slot>
        </b>
    </template>
-->
    <strong v-if='tagType === "strong"'>
        <slot>test</slot>
    </strong>
    <b v-else>
        <slot></slot>
    </b>
</template>

<script>
    // Bold Component help to decorate user input
    export default {
        name: "Bold",
        props: {
            value: String,
            tagType: String
        },
    }
</script>
