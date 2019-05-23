<template>
    <p>
        <span v-html="boldWrapper(value)"></span>
    </p>
</template>

<script>
    export default {
        name: "Paragraph",
        props: {
            value: String,
            tagType: String
        },
        methods: {
            boldWrapper(value) {
                // FIXME: This is vulnerable
                // Because raw string is injectable evil html tag like script tag
                // https://jp.vuejs.org/v2/guide/syntax.html#%E7%94%9F%E3%81%AE-HTML
                if (this.tagType === "strong") {
                    return `<strong>${value}</strong>`
                } else {
                    return `<b>${value}</b>`
                }
            }
        }
    }
</script>
