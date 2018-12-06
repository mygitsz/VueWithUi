<template>
    <div>
        <div
                v-for = "(item, index) in custdet"
                v-bind:item = "item"
                v-bind:index = "index"
                v-bind:itr = "item"
                v-bind:key = "item.fname"
                v-on:removeelement = "custdet.splice(index, 1)">>

        </div>
         <div class = "Table"><div class = "Row"  v-bind:style = "styleobj">
        <div class = "Cell"><p>{{itr.fname}}</p></div>
             <div class = "Cell"><p>{{itr.lname}}</p></div>
        <div class = "Cell"><p>{{itr.addr}}</p></div>
       
         </div>

    </div>
</template>

<script>

    export default {
        name: "ch1",


        props: ['itr', 'index'],
        data: function() {
            return {
                styleobj : {
                    backgroundColor:this.getcolor(),
                    fontSize : 20
                }
            }
        },
        methods:{
            getcolor : function() {
                if (this.index % 2) {
                    return "#FFE633";
                } else {
                    return "#D4CA87";
                }
            }
        }

    }
</script>

<style scoped>

</style>