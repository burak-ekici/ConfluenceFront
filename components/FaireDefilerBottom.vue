<template>
  <div>
    <div class="containeur w-full flex flex-row md:flex-col justify-between px-8 md:px-0 md:py-8 items-center absolute bottom-0 left-0 right-0 md:h-full md:left-0 md:top-O md:bottom-0 md:w-16 ">
      <div class="text-white  transform rotate-180">
          <nuxt-link to="/" class="hidden md:block"><font-awesome-icon :icon="['fas', 'arrow-down']" /></nuxt-link>
      </div>
      <p class="text-white md:block md:transform md:-rotate-90 text-center md:tracking-widest md:pt-0"> FAIRE DEFILER</p>
      <!-- arrow  -->
      <div class="text-white">
          <nuxt-link :to="{path: this.$route.path, hash : hashToScroll }"><font-awesome-icon class="transform scale-150" :icon="['fas', 'long-arrow-down']" /></nuxt-link>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  props: {
    hashToScroll:{
      required : true,
      type: String
    }
  }
}
</script>


<style scoped lang="scss">
@import '@/assets/scss/_variables.scss';
.containeur{
  background-color: $main-color;
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


</style>