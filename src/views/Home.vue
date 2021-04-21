<template>
  <div class="home">
    <hr>
    <h3>3.7v-model基本使用</h3>
    {{name}}
    <CustomerVmodel v-model="name" />
  </div>
</template>

<script>
import CustomerVmodel from "./3Vue基本使用/3-7自定义vmodel";
export default {
  name: "Home",
  data(){
    return{
      name:"123123"
    }
  },
  components: {
    CustomerVmodel,
  },
};
</script>
