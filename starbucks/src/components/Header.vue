<template>
    <header :style="headerStyle">
    <div :style="leftWrapperStyle">
      <Image :imageSrc="imageSrc" :styleValues="imageStyle"></Image>
      <nav :style="navStyle">
        <a v-for="nav in navs">{{ nav.content }}</a>
     </nav>
    </div>
    <div :style="rightWrapperStyle">
      <div :style="btnWrapperStyle">
        <Button :leftIcon="leftIcon" :styleValues="buttonStyle1">Find a store</Button>
        <Button :styleValues="buttonStyle2">Sign in</Button>
        <Button :styleValues="buttonStyle3">Join now</Button>
     </div>
    </div>
  </header>
</template>
<script>
    import Button from './Button.vue'
    import Image from './Image.vue'


    export default{
        components:{
            Button,
            Image
        },
        props:{
            imageSrc: String,
            imageStyle: Object,
            navs: Array,
            buttons: Array,
            navStyle: Object,
            headerStyle: Object,
            leftWrapperStyle: Object,
            rightWrapperStyle: Object,
            btnWrapperStyle: Object,
            leftIcon: String,
            buttonStyle1: Object,
            buttonStyle2: Object,
            buttonStyle3: Object,
        },
    }
</script>