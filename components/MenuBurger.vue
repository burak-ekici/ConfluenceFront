<template>
  <div>
    
    <div @click="toggleMenuBurger" class="md:hidden barContainer absolute right-4 w-16 z-50 h-full flex flex-col items-center justify-center cursor-pointer">
      <div ref="bar1" class="w-8 sm:w-10 h-1 rounded-full bg-white "></div>
      <div ref="bar2"  class="w-8 sm:w-10 h-1 rounded-full bg-white mt-2"></div>
      <div ref="bar3"  class="w-8 sm:w-10 h-1 rounded-full bg-white mt-2"></div>
    </div>
    
    <transition name="MenuBurgerList">
      <div v-if="isMenuOpen" class='w-1/2  md:hidden right-0 h-screen top-16 z-40 fixed bg-black Menu'>
        <nav class="w-full h-full -mt-8 text-center text-white flex flex-col items-center justify-center space-y-16 text-xl font-semibold">
          <nuxt-link to='/'>
            ACCEUIL
          </nuxt-link>
          <nuxt-link to='/services'>
            SERVICES
          </nuxt-link>
          <nuxt-link to='/'>
            A PROPOS
          </nuxt-link>
          <nuxt-link to='/'>
            BLOG
          </nuxt-link>
          <nuxt-link to='/'>
            INTRA
          </nuxt-link>
          <nuxt-link class="border border-white rounded-br-lg ease-out duration-100 rounded-tl-lg p-2 px-3 hover:bg-gray-700 hover:text-white hover:border-white" to='/'>
            CONTACT
          </nuxt-link>
        </nav>
      </div>
    </transition>

  </div>
</template>

<script>
export default {
  props:{
    isMenuBurgerOpen:{type: Boolean}
  },
  data(){
    return {
      isMenuOpen : false,
      isBurgerCross : false
    }
  },
  watch:{
    isMenuBurgerOpen(newValue, oldValue){
      this.isMenuOpen = newValue;
      this.animateBurger();
      this.isBurgerCross = this.isMenuOpen;
    }
  },
  methods: {
    toggleMenuBurger(e){
      e.stopPropagation();
      this.animateBurger();
      this.isBurgerCross = this.isMenuOpen;
      this.isMenuOpen =  this.isMenuOpen ? false : true;
      this.$emit('toggleMenuBurgerStatus' , this.isMenuOpen)
    },
    animateBurger(){
      if(this.isBurgerCross === false){
        this.$nextTick(() => { // When using $refs, must wait for nextTick , la fonction this.$refs est asynchrone, permet d'attendre la reponse avant d'executer le code
          this.$gsap.to(this.$refs.bar1, {rotation: 45, duration: 0.3 , width : 45, y:12});
          this.$gsap.to(this.$refs.bar2, {opacity:0});
          this.$gsap.to(this.$refs.bar3, {rotation: -45, duration: 0.3 , width : 45 , y:-12});
          this.$gsap.to('.barContainer', {rotation: 360, duration: 0.3});
        })
      }else{
        this.$nextTick(() => { // When using $refs, must wait for nextTick , la fonction this.$refs est asynchrone, permet d'attendre la reponse avant d'executer le code
          this.$gsap.to(this.$refs.bar1, {rotation: 0, duration: 0.3 , width : 32, y:0});
          this.$gsap.to(this.$refs.bar2, {opacity:1, duration:0.3});
          this.$gsap.to(this.$refs.bar3, {rotation: 0, duration: 0.3, width : 32 , y:0});
          this.$gsap.to('.barContainer', {rotation: -360, duration: 0.3});
        })
      }
    }
  }
}
</script>

<style scoped>
.Menu{
  font-family: 'Montserrat', sans-serif;
  background-image: linear-gradient(200deg, rgba(171, 171, 171,0.05) 0%, rgba(171, 171, 171,0.05) 23%,rgba(90, 90, 90,0.05) 23%, rgba(90, 90, 90,0.05) 48%,rgba(65, 65, 65,0.05) 48%, rgba(65, 65, 65,0.05) 61%,rgba(232, 232, 232,0.05) 61%, rgba(232, 232, 232,0.05) 100%),linear-gradient(126deg, rgba(194, 194, 194,0.05) 0%, rgba(194, 194, 194,0.05) 11%,rgba(127, 127, 127,0.05) 11%, rgba(127, 127, 127,0.05) 33%,rgba(117, 117, 117,0.05) 33%, rgba(117, 117, 117,0.05) 99%,rgba(248, 248, 248,0.05) 99%, rgba(248, 248, 248,0.05) 100%),linear-gradient(144deg, rgba(64, 64, 64,0.05) 0%, rgba(64, 64, 64,0.05) 33%,rgba(211, 211, 211,0.05) 33%, rgba(211, 211, 211,0.05) 50%,rgba(53, 53, 53,0.05) 50%, rgba(53, 53, 53,0.05) 75%,rgba(144, 144, 144,0.05) 75%, rgba(144, 144, 144,0.05) 100%),linear-gradient(329deg, rgb(0,23,57),rgb(0,23,57));  
}
.MenuBurgerList-enter{
  transform:  translate(100%);
}
.MenuBurgerList-enter-active{
  transition : all 0.5s
}
.MenuBurgerList-leave-to{
  transform:  translate(100%);
}
.MenuBurgerList-leave-active{
  transition : all 0.5s
}



</style>