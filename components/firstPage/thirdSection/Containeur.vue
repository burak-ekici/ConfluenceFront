<template>
  <div ref="section3Containeur" id="third" class="w-full h-screen overflow-hidden relative md:flex pl-20" >
    <div class="section1">
      <FirstPageThirdSectionImage :observed="observerIsActivated" />
    </div>
    <div class="section2">
    <FirstPageThirdSectionDescriptif />
    </div>
    <FaireDefiler hashToScrollBottom="" hashToScrollTop="second" />
  </div>
</template>

<script>
export default {
  data(){
    return{
      observerIsActivated : false
    }
  },
  mounted(){
    const options = {
      root: null,
      rootMargin: '0px',
      threshold:0.2
    }
    const observer = new IntersectionObserver((entries , observer)=>{
      entries.forEach( entry => {
        if(entry.isIntersecting){
          this.observerIsActivated = true
        }
      })
      
    }, options);

    observer.observe(this.$refs.section3Containeur)
  }
}
</script>

<style scoped>
.section1{
  background: url('~/assets/man_tgs_benne.png');
  background-position: center;
}

@media screen and (min-width: 769px){
  .section1{
    width:55%
  }
  .section2{
    width:45%;
  }

}
@media screen and (max-width : 768px){
  #third{
    padding-left: 0px;
    flex-flow:column wrap;
  }
  .section1{
    height: calc(30% - 4rem);
    background-color: red;
    width: 100%;
    margin-top: 2rem;
    background-size: cover;
    position:absolute;
    top:68%;
    background-position: bottom;
  }
  .section2{
    height:70%;
    width:100%;
    position:absolute;
    top:0;
  }
}
@media screen and (max-width : 390px) and (min-resolution : 190dpi){
  .section1{

    margin-top: 3rem;
  }
}



@media screen and (min-width : 800px) and (max-width : 1367px) and (min-resolution : 190dpi){
  #third{
    padding-left: 0px;
    flex-flow:column wrap;
  }
  .section2{
    height:70%;
    width:100%;
    position:absolute;
    top:0
  }
  .section1{
    height: calc(30% - 4rem);
    background-color: red;
    width: 100%;
    margin-top: 2rem;
    background-size: cover;
    position:absolute;
    top:65%;
    background-position: center;
  }
}

</style>


