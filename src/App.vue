<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png">
       <HelloWorld msg="my prog vue.js"/>
        <me1 msg="its just first"/>
       <my1/>
        <todo/>
    </div>
</template>

<script>
   import HelloWorld from './components/HelloWorld.vue'
   import me1 from './components/me1.vue'
   //import Mine1 from './components/mine1'
  // import Ch1 from "./components/ch1";
   import my1 from './components/my1.vue'
   import todo from './components/todo.vue'
   //import Ch1 from "./components/ch1";

   // import comp1 from './components/comp1.vue'
  //  import comp2 from './components/comp2.vue'
  //import mine1 from './components/my1.vue'


    export default {
        name: 'app',
        components: {
            todo,
            my1,


           // Mine1,
            me1,


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
