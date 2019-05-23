<template>
    <p>
        <Bold tagType="tagType">{{value}}</Bold>
    </p>
</template>

<script>
    import Bold from "./Bold.vue";
    export default {
        name: "SafeParagraph",
        components: {
            Bold
        },
        props: {
            value: String,
            tagType: String
        }
    }
</script>
