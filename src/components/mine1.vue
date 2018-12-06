<template>

    <div id = "databinding" style = "">

        <h1>{{ msg }}</h1>
        <h1>Customer Details</h1>
        <span>First Name</span>
        <input type = "text" placeholder = "Enter First Name" v-model = "fname"/>
        <span>Last Name</span>
        <input type = "text" placeholder = "Enter Last Name" v-model = "lname"/>
        <span>Address</span>
        <input type = "text" placeholder = "Enter Address" v-model = "addr"/>
        <button v-on:click = "showdata" v-bind:style = "styleobj">Add</button>
        <br/>
        <br/>


    </div>




</template>

<script>
   // import Ch1 from "./ch1";
    export default {
        name: "mine1",
     //  components: {Ch1},
        props: {
            msg: String,
        },

       data: function() {
            return {
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

            },
        methods :{
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


