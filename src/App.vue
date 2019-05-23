<template>
    <div id="app">
        Input:
        <input v-model="message" placeholder="Evil html:<s>TEST</s>"/>
        <hr/>
        Output:
        <div>
            <label>UnSafeBold</label>
            <UnSafeBold type="strong" :value="message"/>
            <label>SafeBold</label>
            <SafeBold type="strong" :value="message"/>
        </div>
    </div>
</template>

<script>
    import UnSafeBold from './components/UnSafeBold.vue'
    import SafeBold from './components/SafeBold.vue'

    export default {
        name: 'app',
        data: () => {
            return {
                message: ""
            }
        },
        components: {
            UnSafeBold,
            SafeBold
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
