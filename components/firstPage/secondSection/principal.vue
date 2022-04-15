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
@media screen and (max-width : 768px){
  #second{
    padding-left: 0px;
    flex-flow:column wrap;
  }
  .section1{
    height:70%;
    width:100%;
  }
  .section2{
    height: calc(30% - 4rem);
    background-color: red;
    width: 100%;
    margin-top: 2rem;
    background-size: cover;
  }
}
@media screen and (max-width : 390px) and (min-resolution : 190dpi){
  .section2{

    margin-top: 3rem;
  }
}

@media screen and (min-width : 800px) and (max-width : 1367px) and (min-resolution : 190dpi){
  #second{
    padding-left: 0px;
    flex-flow:column wrap;
  }
  .section1{
    height:70%;
    width:100%;
  }
  .section2{
    height: calc(30% - 4rem);
    background-color: red;
    width: 100%;
    margin-top: 2rem;
    background-size: cover;
  }
}
</style>