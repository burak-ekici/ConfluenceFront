<template>
  <div>
    
    <div @click="toggleMenuBurger" class="md:hidden absolute right-4 w-16 z-50 h-full flex flex-col items-center justify-center cursor-pointer">
      <div class="w-8 sm:w-10 h-1 rounded-full bg-white "></div>
      <div class="w-8 sm:w-10 h-1 rounded-full bg-white mt-2"></div>
      <div class="w-8 sm:w-10 h-1 rounded-full bg-white mt-2"></div>
    </div>
    
    <transition name="MenuBurgerList">
      <div v-if="isMenuOpen" class='w-1/2  md:hidden right-0 h-screen top-16 z-40 fixed bg-black Menu'>
        <nav class="w-full h-full -mt-8 text-center text-white flex flex-col items-center justify-center space-y-16 text-xl font-semibold">
          <nuxt-link to='/'>
            ACCEUIL
          </nuxt-link>
          <nuxt-link to='/'>
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
  data(){
    return {
      isMenuOpen : false
    }
  },
  methods: {
    toggleMenuBurger(){
      this.isMenuOpen =  this.isMenuOpen ? false : true
    }
  }
}
</script>

<style scoped>
.Menu{
  font-family: 'Montserrat', sans-serif;
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