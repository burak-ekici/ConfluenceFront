<template>
<div class="w-full MainContainer overflow-hidden" >
  <div class="h-full PageContainer w-full overflow-hidden ">
    <FirstPageFirstSectionLandingPage />
    <FirstPageSecondSectionContaineur />
    <FirstPageThirdSectionContaineur />
  </div>
</div>
</template>

<script>
export default {
  name: 'IndexPage',
  
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/_variables.scss';
@media screen and (min-width: 1920px){
  .PageContainer{
    width:1920px;
  }
  .MainContainer{
    display:flex;
    flex-flow:column wrap;
    align-content:center;
    background-image: linear-gradient(200deg, rgba(171, 171, 171,0.05) 0%, rgba(171, 171, 171,0.05) 23%,rgba(90, 90, 90,0.05) 23%, rgba(90, 90, 90,0.05) 48%,rgba(65, 65, 65,0.05) 48%, rgba(65, 65, 65,0.05) 61%,rgba(232, 232, 232,0.05) 61%, rgba(232, 232, 232,0.05) 100%),linear-gradient(126deg, rgba(194, 194, 194,0.05) 0%, rgba(194, 194, 194,0.05) 11%,rgba(127, 127, 127,0.05) 11%, rgba(127, 127, 127,0.05) 33%,rgba(117, 117, 117,0.05) 33%, rgba(117, 117, 117,0.05) 99%,rgba(248, 248, 248,0.05) 99%, rgba(248, 248, 248,0.05) 100%),linear-gradient(144deg, rgba(64, 64, 64,0.05) 0%, rgba(64, 64, 64,0.05) 33%,rgba(211, 211, 211,0.05) 33%, rgba(211, 211, 211,0.05) 50%,rgba(53, 53, 53,0.05) 50%, rgba(53, 53, 53,0.05) 75%,rgba(144, 144, 144,0.05) 75%, rgba(144, 144, 144,0.05) 100%),linear-gradient(329deg, rgb(0,23,57),rgb(0,23,57));  
  }

}
</style>



