<template>
    <div>
        <input type="text"
            :value="text"
            @input="$emit('ksjdhflksjd', $event.target.value)"
        >
    </div>
</template>

<script>
export default{
    model:{
        prop: "text",
        event: "ksjdhflksjd"
    },
    props:{
        text: String,
        default:{
            return:""
        }
    }
}
</script>
