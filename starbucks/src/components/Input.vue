<template>
    <input :type="type" :style="inputStyle">
</template>

<script>
export default{
    props:{
        type: String,
        inputStyle: Object
    }
}
</script>