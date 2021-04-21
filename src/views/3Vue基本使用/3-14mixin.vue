<template>
  <div>
      {{name}}---{{city}}
      <button @click="showName">Show Name</button>
  </div>
</template>

<script>
import myMixin from "./3-14-1myMixin";
export default {
    mixins:[myMixin],
    data(){
        return{
            name:"huangfl"
        }
    },
    methods:{
        
    }    
}
</script>

<style>

</style>