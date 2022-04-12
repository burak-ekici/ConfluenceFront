<template>
<div class="w-full MainContainer overflow-hidden" >
  <div class="h-full PageContainer w-full overflow-hidden ">
    <FirstPageFirstSectionLandingPage />
    <FirstPageSecondSectionPrincipal />
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
    background-color: #041b31
  }

}
</style>



