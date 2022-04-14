<template>
  <div class=" h-full w-full relative">
    <div class="md:block md:absolute md:top-0 md:bottom-0 md:right-0 md:left-0 fumeeNoir z-10"></div>
    <div class="absolute z-20 Pcontainer">
      <p class="w-full"><img :src="require('~/assets/container_white_icon.png')" alt=""> <span class="number text-3xl ml-4 relative top-2">1784</span> </p>
      <p class="w-full mt-2">Relais terminées</p>
    </div>
  </div>
</template>

<script>
</script>

<style scoped>
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
  font-family: 'Poppins', sans-serif;
  font-size: 2vw;
}
.Pcontainer{
  bottom:6vw;
  right:4vw
}
.number{
  font-weight: 600;
}

@media screen and (max-width : 768px){
  .number{
    font-size:9vw;
  }
  img{
    width:40px;
    display: inline-block;
  }
  p:nth-child(1){
    text-align: left;
  }
  p:nth-child(2){
    font-size: 8vw;
    font-weight: 500;
  }
  
  .Pcontainer{
    top:10%;
    left:4vw
  }
  .fumeeNoir{
    display:block;
    background: linear-gradient(0deg, rgba(0,0,0,0.4) 0%, rgba(0,0,4,0.4) 100%);
    width:100%;
    height:100%
  }
}

</style>