<template>
    <ul id="example-1">
        <li v-for="item in items">
            {{ item.message }}
        </li>
    </ul>
</template>

<script>
    export default {
        name: "comp1",
        data: function () {
            return {
                items: [
                    {message: 'Foo'},
                    {message: 'Bar'}
                ]
            }
        }
    }
</script>

<style scoped>

</style>