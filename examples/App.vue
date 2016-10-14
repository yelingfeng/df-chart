<template>
    <div>
        <p>{{msg}}</p>
        <demo></demo>
    </div>
</template>
<script>
    import demo from "./demo"
    export default {
        name: "app",
        data(){
            return {
                msg: "df-chart"
            }
        },
        components: {
            demo
        },
        mounted(){
        }
    }
</script>
<style>
    body {
        background-color: #000;
    }
</style>