<template>
  <div id="second" class="w-full h-screen overflow-hidden relative md:flex pl-20">

    <div class="section1 h-full w-full">
      <FirstPageSecondSectionDescriptif />
    </div>

    <div class="section2 h-full w-full text-white relative">
      <FirstPageSecondSectionImage />
    </div>

    <FaireDefiler hashToScrollBottom="" hashToScrollTop="first" />
  </div>
</template>

<style scoped>
.section2{
  background: url('~/assets/aerial_entr.jpg');
  background-position: center;
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