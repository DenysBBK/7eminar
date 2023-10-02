<template>
    <button>
        {{ props.text }}
    </button>
</template>
<script setup>
const props = defineProps({
    text:{
        type:String,
        required:true
    }
})
</script>
<style scoped>
button{
    background-color: #0066CC;
    text-align: center;
    border-radius: 980px;
    color: white;
    padding: 18px 32px 18px 32px;
    font-size: 16px;
    font-weight: 700;
    line-height: 20px;
    font-family: Raleway;
}
</style>