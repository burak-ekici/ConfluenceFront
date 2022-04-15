<template>
  <div id="last" class="w-full h-screen overflow-hidden relative md:flex pl-20">
    <FirstPageLastSectionImage />
    <Footer />
    <FaireDefiler hashToScrollBottom="" hashToScrollTop="third" />
  </div>
</template>

<script></script>

<style scoped>
@media screen and (max-width:768px){
  #last{
    padding-left: 0;
  }
}
@media screen and (min-width : 800px) and (max-width : 1367px) and (min-resolution : 190dpi){
  #last{
    padding-left: 0;
  }
}
</style>