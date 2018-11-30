<template>
    <li>
        {{ title }}
        <button v-on:click="$emit('remove')">Remove</button>
    </li>
</template>

<script>
    export default {
        name: "td1",
        props: ['title'],
        data: function () {
            return {
                items: [
                    {title:'asd'}
                ]
            }
        }
    }
</script>

<style scoped>

</style>