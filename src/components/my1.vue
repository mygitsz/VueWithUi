<template>
 <div>
     <div v-for = "(item, index) in custdet"
          v-bind:item = "item"
          v-bind:index = "index"
          v-bind:itr = "item"
          v-bind:key = "item.fname">

     </div>
     <div class = "Table">
         <div class = "Row"  v-bind:style = "styleobj">
             <div class = "Cell"><p>{{itr.fname}}</p></div>
             <div class = "Cell"><p>{{itr.lname}}</p></div>
             <div class = "Cell"><p>{{itr.addr}}</p></div>
             <div class = "Cell"><p><button v-on:click="custdet.splice(index, 1)" :removeelement="custdet.splice(index, 1)" >X</button></p></div>
         </div>
     </div>
     v-on:click = "$emit(\'removeelement\')"
     v-on:remove="todos.splice(index, 1)"
     v-for = "(item, index) in custdet"
     v-bind:item = "item"
     v-bind:index = "index"
     v-bind:itr = "item"
     v-bind:key = "item.fname"

 </div>
</template>

<script>
    export default {
        name: "my1",
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
        },
        data1: function () {
            return{
                data: {
                    fname:'',
                    lname:'',
                    addr : '',
                    custdet:[],
                    styleobj: {
                        backgroundColor: '#2196F3!important',
                        cursor: 'pointer',
                        padding: '8px 16px',
                        verticalAlign: 'middle',
                    }
                }
            }
        },

            showdata : function() {
                this.custdet.push({
                    fname: this.fname,
                    lname: this.lname,
                    addr : this.addr
                });
                this.fname = "";
                this.lname = "";
                this.addr = "";
            }


    }

</script>

<style scoped>
    #databinding{
        padding: 20px 15px 15px 15px;
        margin: 0 0 25px 0;
        width: auto;
    }
    span, option, input {
        font-size:20px;
    }
    .Table{
        display: table;
        width:80%;
    }
    .Title{
        display: table-caption;
        text-align: center;
        font-weight: bold;
        font-size: larger;
    }
    .Heading{
        display: table-row;
        font-weight: bold;
        text-align: center;
    }
    .Row{
        display: table-row;
    }
    .Cell{
        display: table-cell;
        border: solid;
        border-width: thin;
        padding-left: 5px;
        padding-right: 5px;
        width:30%;
    }
</style>