<template>
        <cross-fade-viewer claas="cfv"
        :availableImages="[
          {title: 'Some Title A', sourceUrl: 'https://scontent-frx5-1.xx.fbcdn.net/v/t31.18172-8/16107459_10154992264123000_2397801684756506059_o.jpg?_nc_cat=111&ccb=1-5&_nc_sid=dd9801&_nc_eui2=AeFLTVfKaQHwyEpNNmsvfuyEBNApW8N3nwcE0Clbw3efB8RvKi8xHIz9busi99nzPc8&_nc_ohc=XB2PzpKeprgAX-nalRa&tn=D78IzNp5aR4YTKNY&_nc_ht=scontent-frx5-1.xx&oh=00_AT9M8DmHTQ5Wtvew9igrLSLCn6UnmcVjxtCgtbeo19uHVA&oe=625DBCE4&dl=1', opacity: 1},
          {title: 'Some Title B', sourceUrl: 'https://scontent-frt3-1.xx.fbcdn.net/v/t39.30808-6/242782246_10159887752938000_4763621858983244061_n.jpg?_nc_cat=102&ccb=1-5&_nc_sid=8024bb&_nc_eui2=AeH3Gehd4RjOijhJ03-OzpVWr3ADleM8wKmvcAOV4zzAqSbLGlNgH1f9i2m10CO94BI&_nc_ohc=rcHlkuC1EBYAX8t7mQ6&_nc_ht=scontent-frt3-1.xx&oh=00_AT9Dj-FUcMn7UyfYMMdVdg2QP0dd4za3xCJhSU1FOPYrpQ&oe=623DC47F&dl=1', opacity: 1},
         ]"
        :displayedImages="[
          {title: 'Some Title D', sourceUrl: 'https://scontent-frx5-1.xx.fbcdn.net/v/t1.6435-9/46741580_10157008357303000_2444844939939414016_n.jpg?_nc_cat=111&ccb=1-5&_nc_sid=dd7718&_nc_eui2=AeEHouku0WGApI5PBJMhwm2qJd8eU1WzY4Il3x5TVbNjgvf7o0Ciyy0ysfaJ2AABCUw&_nc_ohc=YvxF_cMQU54AX_C8xE3&tn=D78IzNp5aR4YTKNY&_nc_ht=scontent-frx5-1.xx&oh=00_AT_y6yL5gTqXXyVItQpR9QTraTX4QztYKRKXT_XQKaNirw&oe=625DE4CB&dl=1', opacity: 1},
         ]"
        :integratedGallery="true"
        />
</template>

<script>
 //const results1 = await fetch(`https://api.instagram.com/v1/users/self/media/recent/?access_token=` + this.access_token, {
  //      method: 'GET',})
import CrossFadeViewer from '@cross-fade-viewer/vue-component';
export default {
  name: 'App',
  components: {
    CrossFadeViewer
  }
}
</script>

<style>
.cfv { height:100vh;
width:100vw;}

</style>