<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png">
       <HelloWorld msg="my prog vue.js"/>
        <mine1 msg="its first"/>
        <mine1 msg="progecs"/>

    </div>
</template>

<script>
   import HelloWorld from './components/HelloWorld.vue'
   import Mine1 from "./components/mine1";
   // import comp1 from './components/comp1.vue'
  //  import comp2 from './components/comp2.vue'
  //import my1 from './components/my1.vue'


    export default {
        name: 'app',
        components: {
            Mine1,
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
