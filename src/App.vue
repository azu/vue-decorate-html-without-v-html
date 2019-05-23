<template>
    <div id="app">
        Input:
        <input v-model="message" placeholder="Evil html:<s>TEST</s>"/>
        <hr/>
        Output:
        <div>
            <label>UnSafeParagraph</label>
            <UnSafeParagraph type="strong" :value="message"/>
            <label>SafeParagraph</label>
            <SafeParagraph type="strong" :value="message"/>
        </div>
    </div>
</template>

<script>
    import UnSafeParagraph from './components/UnSafeParagraph.vue'
    import SafeParagraph from './components/SafeParagraph.vue'

    export default {
        name: 'app',
        data: () => {
            return {
                message: ""
            }
        },
        components: {
            UnSafeParagraph,
            SafeParagraph
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
