<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <tablel></tablel>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import tablel from "@/components/table.vue";

export default {
  name: "home",
  components: {
    HelloWorld,
    tablel
  }
};
</script>
