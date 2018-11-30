<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png">
        <HelloWorld msg="mos ravani ablah bi shoooouuuuuuurrrrrrrrr"/>
        <comp1 />
        <comp2/>
    </div>
</template>

<script>
    import HelloWorld from './components/HelloWorld.vue'
    import comp1 from './components/comp1.vue'
    import comp2 from './components/comp2.vue'


    export default {
        name: 'app',
        components: {
            HelloWorld,comp1,comp2
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
