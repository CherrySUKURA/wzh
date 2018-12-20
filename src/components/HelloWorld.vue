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
          trigger: "item",
          formatter: "{a} <br/>{b} : {c} ({d}%)"
        }, //提示框
        series: [
          {
            type: "pie",
            data: [
              {
                name: this.tableData[0].name,
                value: this.tableData[0].zip
              },
              {
                name: this.tableData[1].name,
                value: this.tableData[1].zip
              },
              {
                name: this.tableData[2].name,
                value: this.tableData[2].zip
              },
              {
                name: this.tableData[3].name,
                value: this.tableData[3].zip
              },
              {
                name: this.tableData[4].name,
                value: this.tableData[4].zip
              },
              {
                name: this.tableData[5].name,
                value: this.tableData[5].zip
              },
              {
                name: this.tableData[6].name,
                value: this.tableData[6].zip
              }
            ]
          }
        ]
      });
    }
  },
  props: {
    tableData: {
      type: Array,
      default: function() {
        return [];
      }
    }
  }
};
</script>


