<template>
  <div class="imageInputs" style="padding: 16px;">
    <label>Title</label>
    <input id="imageTitle" v-model="imageTitle">
    <label>URL</label>
    <input id="imageSource" v-model="imageSource">
    <button @click="addItemToArray">Add Image</button>
  </div>
  <div class="component">
    <cross-fade-viewer
    :availableImages=imageArray
    :integratedGallery="true"
    />
    </div> 
</template>

<script>
 //const results1 = await fetch(`https://api.instagram.com/v1/users/self/media/recent/?access_token=` + this.access_token, {
  //      method: 'GET',})
import CrossFadeViewer from '@cross-fade-viewer/vue-component';
export default {
  name: 'App',
  components: {
    CrossFadeViewer
  },
  props: {
    imageTitle : { type: String, default: ""},
    imageSource : { type: String, default: ""},
  },
  setup(props) {
    // examples:
    // {title: 'Silhouette filter', sourceUrl: 'https://scontent-ham3-1.xx.fbcdn.net/v/t39.30808-6/277231571_10160242135578000_4882166319159946334_n.jpg?_nc_cat=107&ccb=1-5&_nc_sid=0be424&_nc_eui2=AeHgmH7pquttWajhMT8tLSoQObAChuN-hvU5sAKG436G9RgkGBxrjxkEs3Xtcj2DSwI&_nc_ohc=DvMKONEYmKsAX9q7xwr&_nc_ht=scontent-ham3-1.xx&oh=00_AT-PcZvC6gcWUCh_aeKnL4Vt8awU4lKpZeiND1K3pduuwA&oe=623F549C&dl=1', opacity: 1},
    // {title: 'Fine art filter', sourceUrl: 'https://scontent-ham3-1.xx.fbcdn.net/v/t39.30808-6/277166176_10160242133778000_6211252922917178425_n.jpg?_nc_cat=104&ccb=1-5&_nc_sid=0be424&_nc_eui2=AeGUOBTpYJkaKsBwevTpk50BOeQEW8yRvHM55ARbzJG8cxB4p9faWMK5E_ThQOP2T5M&_nc_ohc=7fqi3ruuWzoAX95Cr9h&_nc_ht=scontent-ham3-1.xx&oh=00_AT8O09L_zFy8Crhu8hxKTMakiNOFSodflAROcDZV0G2uug&oe=624105EE&dl=1', opacity: 1},
    // {title: 'Customized', sourceUrl: 'https://scontent-frt3-1.xx.fbcdn.net/v/t39.30808-6/277250965_10160242158308000_6813227152296581367_n.jpg?_nc_cat=106&ccb=1-5&_nc_sid=0be424&_nc_eui2=AeEBUNzhWPI6lUA-HuGoyycjjETd6IhTFdyMRN3oiFMV3HzHLKrfYeDJzXZIGBO8_q0&_nc_ohc=Ci2IfkxXPc4AX-xUOeT&_nc_ht=scontent-frt3-1.xx&oh=00_AT94TzkSJvUTlbsSlxH-bc2LVYUDYtmrd0WsWoHqQgs-Zg&oe=623F9AB2&dl=1', opacity: 1},
    // {title: 'Original', sourceUrl: 'https://scontent-ham3-1.xx.fbcdn.net/v/t39.30808-6/277244908_10160242132383000_595372705761649019_n.jpg?_nc_cat=111&ccb=1-5&_nc_sid=0be424&_nc_eui2=AeEAuugqXiC1Nsg_8I-bo1JjS1Gb9mY-4U5LUZv2Zj7hTh2DCWBuKk9OQqZLFARfmeo&_nc_ohc=829-V0pG58EAX8wJ1Al&_nc_ht=scontent-ham3-1.xx&oh=00_AT9HpOEBaTg7nD7biiAd0MnAc0vI_vxY_RTcoOV6n3JLoA&oe=624116C6&dl=1', opacity: 1},

    const imageArray = [];

    function addItemToArray() {
      const title = props.imageTitle;
      const sourceUrl = props.imageSource;
      imageArray.push({
        title,
        sourceUrl,
        opacity: 1,
      });
    };

    return {
      addItemToArray,
      imageArray,
    };
  },
};
</script>

<style>


</style>