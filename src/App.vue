<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png">
       <HelloWorld msg="my prog vue.js"/>
        <me1 msg="its first"/>


    </div>
</template>

<script>
   import HelloWorld from './components/HelloWorld.vue'
   import me1 from './components/me1.vue'

   // import comp1 from './components/comp1.vue'
  //  import comp2 from './components/comp2.vue'
  //import my1 from './components/my1.vue'


    export default {
        name: 'app',
        components: {
            me1,
            //my1,
            HelloWorld
           // comp1,comp2
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
