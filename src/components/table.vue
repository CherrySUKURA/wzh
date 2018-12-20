<template>
  <el-table :data="tableData3" style="width: 100%">
    <el-table-column prop="name" label="姓名" width="120"></el-table-column>
    <el-table-column prop="zip" label="邮编" width="120"></el-table-column>
    <HelloWorld :tableData="tableData3" :slot-scope="scope"></HelloWorld>
  </el-table>
</template>

<script>
import HelloWorld from "@/components/HelloWorld.vue";
export default {
  data() {
    return {
      tableData3: [
        {
          name: "A",
          zip: 20000
        },
        {
          name: "B",
          zip: 20000
        },
        {
          name: "B",
          zip: 20333
        },
        {
          name: "D",
          zip: 20088
        },
        {
          name: "E",
          zip: 20666
        },
        {
          name: "F",
          zip: 20033
        },
        {
          name: "G",
          zip: 20035
        }
      ]
    };
  },
  components: {
    HelloWorld
  }
};
</script>