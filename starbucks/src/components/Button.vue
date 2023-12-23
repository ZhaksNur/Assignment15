<template>
    <button :style="styleValues">
        <img v-if="leftIcon" :src="leftIcon"/>
        <slot></slot>
        <img v-if="rightIcon" :src="leftIcon"/>
        </button>
</template>

<script>
export default{
    props: {
        leftIcon: String,
        styleValues: Object,
        rightIcon: String
    },
}
</script>