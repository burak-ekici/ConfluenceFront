<template>
  <div>
    <div ref="containeur" class="containeur w-full flex flex-row md:flex-col justify-between px-8 md:px-0 md:py-8 items-center absolute bottom-0 left-0 right-0 md:h-full md:left-0 md:bottom-0 md:w-20 ">
      
      <div ref="topArrow"  class="text-white  transform rotate-180">
          <nuxt-link v-if="!removeTopArrow" :to="{path: this.$route.path, hash : hashToScrollTop }" class="hidden md:block"><font-awesome-icon class="transform scale-150" :icon="['fas', 'long-arrow-down']" /></nuxt-link>
      </div>
      
      <p class="texteDefiler text-white md:block md:transform md:-rotate-90 text-center md:tracking-widest md:pt-0"> FAIRE DEFILER</p>
      <!-- arrow  -->
      <div class="text-white">
          <nuxt-link v-if="!removeBottomArrow" :to="{path: this.$route.path, hash : hashToScrollBottom }"><font-awesome-icon class="transform scale-150" :icon="['fas', 'long-arrow-down']" /></nuxt-link>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  data(){
    return{
      removeTopArrow : false,
      removeBottomArrow : false
    }
  },
  props: {
    hashToScrollTop:{
      required : true,
      type: String
    },
    hashToScrollBottom:{
      required : true,
      type: String
    },
  },
  created(){
    if(this.hashToScrollTop === ''){
      this.removeTopArrow = true 
    }
    if(this.hashToScrollBottom === ''){
      this.removeBottomArrow = true 
    }
  }
}
</script>


<style scoped lang="scss">
@import '@/assets/scss/_variables.scss';
.containeur{
  background-color: $main-color;
  height:100%;
  padding-top:6rem
}

p{
  font-family: 'Montserratscss', sans-serif;
  font-weight:100;
  color:rgba(255,255,255,0.6);
  font-size: 0.8rem;
  letter-spacing: 2px;
}

@media screen and (max-width: 767px){
  .containeur{
    height:8%
  }
}

@media screen and (min-width: 1024px){
  .containeur{
    height:100%;
    padding-top: 7.5rem;
  }
}

@media only screen and ( min-resolution: 190dpi) and (max-width: 768px){
  .containeur{
    bottom:0;
    left:0;
    right:0;
    width:100%;
    height:8%;
    padding : 2rem 0 ;
    display:flex;
    justify-content: space-between;
    flex-flow:row nowrap;
    padding: 0 2rem;
    z-index: 10;
  }
  .texteDefiler{
    transform: rotate(0);
  }
}
</style>