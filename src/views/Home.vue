<template>
  <div class="home">
    <hr />
    <h3>3.7v-model基本使用</h3>
    {{ name }}
    <CustomerVmodel v-model="name" />
    <hr />
    <h3>$nextTick使用</h3>
    <NextTick v-model="name" />
    <hr />
    <h3>SlotDemo使用</h3>
    <SlotDemo :url="url">
      <template v-slot="slotProps">
        {{slotProps}}
      </template>
    </SlotDemo>
  </div>
</template>

<script>
import CustomerVmodel from "./3Vue基本使用/3-7自定义vmodel";
import NextTick from "./3Vue基本使用/3-8$nextTick";
import SlotDemo from "./3Vue基本使用/3-9Slot的基本使用";

export default {
  name: "Home",
  data() {
    return {
      name: "123123",
      content: "网站地址",
      url: "https://www.baidu.com",
      webSite: {
        name: "前端技术分享",
      },
    };
  },
  components: {
    CustomerVmodel,
    NextTick,
    SlotDemo,
  },
};
</script>
