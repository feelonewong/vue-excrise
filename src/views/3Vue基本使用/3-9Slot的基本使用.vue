<template>
  <div>
    <h4>基本使用、具名插槽、作用域插槽、</h4>
    <!-- <a :href="url">
            <slot>
                如果没有传值，默认显示空值
            </slot>
        </a> -->
        <a :href="url">
            <slot :slotData="webSite">
                {{webSite.name}}
            </slot>
        </a>
  </div>
</template>

<script>
export default {
  props: {
    url: {
      type: String,
    },
  },
  data() {
    return {
      webSite: {
        name: "前端技术分享",
      },
    };
  },
};
</script>
