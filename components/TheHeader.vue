<template>
<div class="premierContaineur w-full lg:h-24 h-16 absolute top-0">
  <div class='secondContaineur w-full lg:h-24 h-16 flex bg-main-color fixed z-50'>
      
      <div class='lg:w-1/3 w-1/2 ml-8 md:ml-20 h-full flex flex-col justify-center text-white'>
        <h1 class=' text-xl sm:text-2xl font-black tracking-wide conff'>CONFLUENCE</h1>
        <h2 class=' text-md sm:text-xl font-light italic -mt-2 transpp'>TRANSPORTS</h2>
      </div>

      <MenuBurger :isMenuBurgerOpen="isMenuBurgerOpen" @toggleMenuBurgerStatus='toggleMenuBurgerStatus' />
      
      <div class='hidden md:w-2/3 w-1/2 md:flex items-center pr-10'>
        <nav class="w-full text-center text-white flex items-center justify-between lg:justify-around text-sm font-semibold">
          <NuxtLink class="hover:text-black ease-out duration-100" to='/'>
            ACCEUIL
          </NuxtLink>
          <NuxtLink to='/services'>
            SERVICES
          </NuxtLink>
          <NuxtLink to='/r'>
            A PROPOS
          </NuxtLink>
          <NuxtLink to='/z'>
            BLOG
          </NuxtLink>
          <NuxtLink to='/e'>
            INTRA
          </NuxtLink>
          <NuxtLink class="border contact py-2 px-3 tracking-wider rounded-tl-md rounded-br-md" to='/n'>
            CONTACT
          </NuxtLink>
        </nav>
      </div>
      
  </div>
</div>
</template>

<script>
export default {
  props:{
    isMenuBurgerOpen:{
      type:Boolean
    }
  },
  methods:{
    toggleMenuBurgerStatus(value){
      this.$emit('toggleMenuBurgerStatus' , value)
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/_variables.scss';
.bg-main-color{
  background-color:  $main-color
}
.contact{
  font-size:12px
}
.nuxt-link-exact-active {
  font-weight:900;
  font-size : 16px;
  opacity: 0.8
}

a:hover:not(.nuxt-link-active){
  color:#023564;
}
.contact:hover{
  background:#0378e5;
}
nav{
  font-family: 'Poppins', sans-serif;
}
.conff{
  font-family: 'Montserrat', sans-serif;
  font-weight: 900;
}
.transpp{
  font-family: 'Montserrat', sans-serif;
  font-weight: 200;
  letter-spacing: 5px;
}
@media screen and (max-width: 640px){
  .transpp{
    letter-spacing: 4.6px;
  }
}

@media screen and (min-width: 1920px){
  .premierContaineur{
    display:flex;
    justify-content: center;
  }
  .secondContaineur{
    max-width:1920px;
  }

}


</style>
