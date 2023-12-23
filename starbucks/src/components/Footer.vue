<template>
    <footer>
        <Banner :banners="banners" :textContentStyle="textContentStyle" :textWrapperStyle="textWrapperStyle" :bannerStyle="bannerStyle" :pStyle="pStyle"></Banner>
    </footer>
</template>
<script>

import Banner from './Banner.vue'

export default{
    props:{
        banners: Array,
    },
    components:{
        Banner,
    },
    data(){
        return{
            bannerStyle:{
                position:'relative',
                margin: '60px 0 60px 0',
            },
            textContentStyle:{
                width:'100%',
                height: 'auto',
                position: 'relative',
                display: 'flex',
                flexDirection: 'column',
                justifyContent: 'center',
                alignItems: 'center'
            },
            textWrapperStyle:{
                width: '45%'
            },
            pStyle:{
                fontSize: '11px',
                textAlign: 'center'
            }
        }
    }
}
</script>