<template>
    <div>
        <ul ref="listRef">
            <li v-for="item in list" :key="item">
                {{item}}
            </li>
        </ul>
        <button @click="handleAdd">add</button>
    </div>
</template>

<script>
export default {
    data(){
        return{
            list:["a","b","c"]
        }
    },
    methods:{
        handleAdd(){
            this.list.push(`${Date.now()}`);
            //解决DOM渲染不会立即实现问题，多次修改DOM 只会执行一次
            this.$nextTick( ()=>{
            console.log(this.$refs.listRef.childNodes.length, "length")

            } )

        }
    }
}
</script>