<template>

    <html>
    <head>
        <title>VueJs Instance</title>

    </head>
    <body>
    <div class="h">
        <h1>{{ msg }}</h1>

    </div>
    <style scoped>

        #databinding{
            padding: 20px 15px 15px 15px;
            margin: 0 0 25px 0;
            width: auto;
            background-color: #e7e7e7;
        }
        span, option, input {
            font-size:25px;
        }

    </style>
    <div id = "databinding" style = "">
        <h1>Currency Converter</h1>
        <span>Enter Amount:</span><input type = "number" v-model.number = "amount" placeholder = "Enter Amount" /><br/><br/>
        <span>Convert From:</span>

    </div>

    </body>
    </html>
</template>

<script>
    export default {
        name: "mine1",
        props: {
            msg: String,

        },
      //  el: '#databinding',
      //  data: {

            data: function () {
            return{
                name:'',
                currencyfrom : [
                    {name : "USD", desc:"US Dollar"},
                    {name:"EUR", desc:"Euro"},
                    {name:"INR", desc:"Indian Rupee"},
                    {name:"BHD", desc:"Bahraini Dinar"}
                ],
                convertfrom: "INR",
                convertto:"USD",
                amount :""
            }

            }
     //   },
    }

</script>

<style scoped>

    #databinding{
        padding: 20px 15px 15px 15px;
        margin: 0 0 25px 0;
        width: auto;
        background-color: #e7e7e7;
    }
    span, option, input {
        font-size:25px;
    }

</style>


