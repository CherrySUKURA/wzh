<template>
  <div id="main" style="width: 600px;height:400px;"></div>
</template>
<script >
//初始化echarts
export default {
  //在vue渲染到都没元素时启用回调函数
  mounted() {
    this.draw();
  },
  methods: {
    //指定图表的配置项和数据
    draw() {
      var echarts = require("echarts");
      //导入echar依赖，在node_modules里面，这里说一下import和require的区别，import需要具体到相对地址，而require则不用，会自动安装
      var myChart = echarts.init(document.getElementById("main"));
      myChart.setOption({
        title: { text: "杭州未来一个星期天气走势" },
        tooltip: {
            
        }, //提示框
        series: [
          {
               type: 'pie',
                data: [
                    {name: 'A', value: 1212},
                    {name: 'B', value: 2323},
                    {name: 'C', value: 1919}
                ]
          }
        ]
      });
    }
  }
};
</script>


