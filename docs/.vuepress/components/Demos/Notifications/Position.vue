<template lang="html">
  <div class="con-notifications-position">
    <vs-button @click="$vs.notify({title:'Position Default',text:'Lorem ipsum dolor sit amet, consectetur',color:'primary'})" vs-type="primary-flat">Position Default</vs-button>

    <vs-button @click="$vs.notify({title:'Position top-right',text:'Lorem ipsum dolor sit amet, consectetur',color:'success',position:'top-right'})" vs-type="success-flat">Position Top Right</vs-button>

    <vs-button @click="$vs.notify({title:'Position top-left',text:'Lorem ipsum dolor sit amet, consectetur',color:'danger',position:'top-left'})" vs-type="danger-flat">Position Top Left</vs-button>

    <vs-button @click="$vs.notify({title:'Position bottom-left',text:'Lorem ipsum dolor sit amet, consectetur',color:'warning',position:'bottom-left'})" vs-type="warning-flat">Position Bottom Left</vs-button>

    <vs-button @click="$vs.notify({title:'Position bottom-center',text:'Lorem ipsum dolor sit amet, consectetur',color:'dark',position:'bottom-center'})" vs-type="dark-flat"> Position Bottom Center</vs-button>

    <vs-button @click="notiAzarCenter()" vs-type="success-gradient">Position Top Center Color Al Azar</vs-button>
  </div>
</template>

<script>
export default {
  methods:{
    notiAzarCenter(){
      function getRandomInt(min, max) {
        return Math.floor(Math.random() * (max - min)) + min;
      }
      let color = `rgb(${getRandomInt(0,255)},${getRandomInt(0,255)},${getRandomInt(0,255)})`

      this.$vs.notify({title:'Position top-center',text:'Lorem ipsum dolor sit amet, consectetur',color:color,position:'top-center'})
    }
  }
}
</script>

<style lang="css">
.con-notifications-position {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
}
</style>
