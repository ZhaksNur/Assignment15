<script>
import Image from './components/Image.vue'
import starbuckImage from './assets/starbucks.svg'
import Button from './components/Button.vue'
import locationImage from './assets/location.svg'
import image1 from './assets/img1.jpg'
import Banner from './components/Banner.vue'
import image2 from './assets/img2.jpg'
import image3 from './assets/img3.png'
import image4 from './assets/img4.png'
import image5 from './assets/img5.jpg'
import image6 from './assets/img6.jpg'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default{
  components:{
    Image,
    Button,
    Banner,
    Header,
    Footer
  },
  data(){
    return{
      starbuckImage: starbuckImage,
      locationImage: locationImage,
      imageStyle:{
        width: '50px',
      },
      banners: [{title: 'Last-minute merry', mainText: 'A Starbucks eGift is quick to send and a joy to receive. Perfect for anyone on your list.', buttonText: 'Send an eGift' , rightImage: image1},
                {title: 'Half off for the holidays', mainText: 'Feeling festive? Starbucks® Rewards members can get half off a drink on Thursday afternoons (12-6 PM) in December.*', buttonText: 'Join for free', leftImage: image2},
                {title: 'The game is on!', mainText: 'There’s still time to play Starbucks for Life! This year we’re giving away over 10 million prizes.**', buttonText: 'Play now', rightImage: image3},
                {title: 'Cozy new chai', mainText: 'Today calls for a Gingerbread Oatmilk Chai with warming spices and the festive flavor of gingerbread.', buttonText: 'Order now', leftImage: image4},
                {title: 'Hooray for brulée', mainText: '’Tis the season for our Caramel Brulée Latte with a crunchy, caramelly topping.', buttonText: 'Order now', rightImage: image5},
                {title: '50% off select gifts*** for them and you', mainText: 'Stop by and save on festive coffee favorites, cold cups, tumblers and more. Now through Dec. 25.', buttonText: 'Find a store', leftImage: image6}
              ],
      bannerStyle:{
        width: '100%',
        heigth: 'auto',
        display: 'flex',
        backgroundColor: '#dc0032',
        marginTop: '30px',
      },
      imgBannerStyle:{
        width: '50%'
      },
      buttonStyle1:{
        width: '110px',
        border: 'none',
        display: 'flex',
        justifyContent: 'space-between',
        backgroundColor: 'white',
        fontWeight: 'bold',
        fontSize: '12px',
        padding: '0px',
        cursor: 'pointer',
      },
      buttonStyle2: {
        width: '75px',
        padding: '7px',
        backgroundColor: 'white',
        color: 'black',
        border: '1px solid black',
        borderRadius: '30px',
        fontWeight: 'bold',
        fontSize: '12px',
        cursor: 'pointer',
      },
      buttonStyle3: {
        width: '85px',
        padding: '7px',
        backgroundColor: 'black',
        color: 'white',
        border: '1px solid black',
        borderRadius: '30px',
        fontWeight: 'bold',
        fontSize: '12px',
        cursor: 'pointer',
      },
      textContentStyle:{
        width: '50%',
        heigth: '100%',
        display: 'flex',
        flexDirection: 'column',
        alignItems: 'center',
        justifyContent: 'center'
      },
      textWrapperStyle:{
        width: '500px',
        position: 'relative',
        display: 'flex',
        flexDirection: 'column',
        alignItems: 'center',
        justifyContent: 'center',
        textAlign:'center',
      },
      h1Style:{
        fontSize: '40px',
        color: '#fff',
        fontWeight: '600'
      },
      pStyle:{
        fontSize: '20px',
        color: 'white',
        fontWeight: '500'
      },
      bannerButtonStyle:{
        width: 'auto',
        padding: '10px',
        backgroundColor: '#dc0032',
        color: 'white',
        border: '1px solid white',
        borderRadius: '30px',
        fontWeight: '600',
        fontSize: '12px',
        cursor: 'pointer',
      },
      navs:[{content: 'MENU'}, {content: 'REWARDS'}, {content: 'GIFT CARDS'}],
      navStyle:{
        position: 'relative',
        display: 'flex',
        width: '320px',
        margin: '20px',
        textTransform: 'uppercase',
        fontWeight: 'bold',
        justifyContent: 'space-between',
        fontSize: '14px',
      },
      headerStyle:{
        width:'100%',
        position: 'relative',
        display: 'flex',
        height: '80px',
        justifyContent: 'center',
        boxShadow: '0px 2px 2px 0px rgb(196, 195, 195)'
      },
      leftWrapperStyle:{
        width: '48%',
        display: 'flex',
        alignItems: 'center',
        justifyContent: 'flex-start'
      },
      rightWrapperStyle:{
        width: '48%',
        display: 'flex',
        alignItems: 'center',
        justifyContent: 'flex-end'
      },
      btnWrapperStyle:{
        width: '55%',
        position: 'relative',
        display: 'flex',
        justifyContent: 'space-between',
        alignItems: 'center',
      },
      footerBanners:[{mainText:'*At participating stores. Offer applies to drinks prepared by baristas, including coffee and tea. Limit one drink per member. Cannot be combined with other offers or promotions. This offer is exclusive to you and this Starbucks Rewards account and cannot be reproduced, transferred or used by anyone else.'},
                     {mainText: '**NO PURCHASE NECESSARY. Participating stores only. Starbucks Partners (employees) are not eligible to win prizes. Ends 12/31/23. To play and for Official Rules, visit https://www.starbucksforlife.com/.'},
                     {mainText: '***© 2023 Warner Bros. Entertainment Inc. All Rights Reserved. Rated PG-13.'},
                     {mainText: '****Valid through 12/25 at participating stores. Offer good on Starbucks Reserve® Christmas 2023; excludes other Starbucks Reserve® coffees and nonseasonal packaged coffees, purchases of Starbucks Cards and Starbucks Card reloads, and nonseasonal merchandise collections. Cannot be combined with other offers or discounts. Limited to stock on hand.'}
      ],
    }
  }
}
</script>

<template>
  <Header :imageSrc="starbuckImage" :imageStyle="imageStyle" :navs="navs" :navStyle="navStyle" :headerStyle="headerStyle" :leftWrapperStyle="leftWrapperStyle" :rightWrapperStyle="rightWrapperStyle" :btnWrapperStyle="btnWrapperStyle" :buttons="buttons" :buttonsStyles="buttonsStyles" :buttonStyle1="buttonStyle1" :buttonStyle2="buttonStyle2" :buttonStyle3="buttonStyle3" :leftIcon="locationImage"></Header>
  <Banner :banners="banners" :bannerStyle="bannerStyle" :imageStyle="imgBannerStyle" :textContentStyle="textContentStyle" :h1Style="h1Style" :textWrapperStyle="textWrapperStyle" :pStyle="pStyle" :buttonStyle="bannerButtonStyle"></Banner>
  <Footer :banners="footerBanners"></Footer>
</template>

<style>
*{
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}
a:hover{
color: rgb(82, 106, 82);
}
</style>
