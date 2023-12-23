<template>
    <img :src="imageSrc" :style="styleValues"/>
</template>

<script>
export default{
    props:{
        imageSrc: String,
        styleValues: Object
    }
}
</script>