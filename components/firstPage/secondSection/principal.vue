<template>
  <div id="second" class="w-full h-screen overflow-hidden relative md:flex pl-20">

    <div class="section1 h-full w-full"></div>

    <div class="section2 h-full w-full text-white relative">
      <div class="hidden md:block md:absolute md:top-0 md:bottom-0 md:right-0 md:left-0 fumeeNoir z-10"></div>
      <div class="absolute z-20 Pcontainer">
        <p class="w-full"><img :src="require('~/assets/container_white_icon.png')" alt=""> <span class="number text-3xl ml-4 relative top-2">1784</span> </p>
        <p class="w-full mt-2">Relais terminées</p>
      </div>
    </div>

    <FaireDefiler hashToScrollBottom="" hashToScrollTop="first" />
  </div>
</template>

<style scoped>
.section2{
  background: url('~/assets/aerial_entr.jpg');
}
.fumeeNoir{
  background: linear-gradient(0deg, rgba(0,0,0,0.7) 0%, rgba(0,0,4,0) 30%, rgba(0,0,4,0) 100%);
}

img{
  width:40px;
  display: inline-block;
}
p{
  font-family: 'Montserrat', sans-serif;
}
p:nth-child(1){
  text-align: right;
}
p:nth-child(2){
  font-size: 2vw;
}
.Pcontainer{
  bottom:4vw;
  right:4vw
}
.number{
  font-weight: 600;
}
@media screen and (min-width: 769px){
  .section1{
    width:45%;
  }
  .section2{
    width:55%
  }
}
</style>