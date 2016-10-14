<template>
    <div>
        <div class="box" id="box2"></div>
    </div>
</template>
<script>
    import dfChart from "../src/index"
    export default {
        name: "demo",
        data(){
            return {
                barData: [{name: '数据1', value: 10, category: "分类A", info: "AAAACCCC"},
                    {name: '数据1', value: 20, category: "分类A"},
                    {name: '数据1', value: 30, category: "分类A"},
                    {name: '数据2', value: 30, category: "分类B"},
                    {name: '数据2', value: 15, category: "分类B"},
                    {name: '数据2', value: 25, category: "分类B"},
                    {name: '数据3', value: 25, category: "分类C"},
                    {name: '数据3', value: 35, category: "分类C"},
                    {name: '数据3', value: 45, category: "分类C"}]
            }
        },
        mounted(){
            this.bar01 = new dfChart.Bar({
                el: document.querySelector("#box2"),
                sub: 'base',
                props: {
                    specialProps: {
                        ylName: "产品",
                        ylUnit: "(个)",
                        xName: "横",
                        xUnit: "(单位)"
                    },
                    commonProps: {
                        showLegend: true,
                        legendPositon: 4,
                        rotate: "45"
                    }
                }
            }).render(this.barData)
        }

    }
</script>
<style>
    .box {
        width: 500px;
        height: 400px;
    }
</style>