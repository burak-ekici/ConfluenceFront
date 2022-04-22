<template>
<div class="containeur bg-white h-screen pt-16 w-full relative">
  <div class="flex flex-col md:flex-row w-full h-full md:px-32 lg:px-64 space-x-4 ">

    <div class="md:w-1/3 w-full h-full p-8">
      <div class="bg-white h-full md:h-full w-full rounded-xl block1 relative">
        <nuxt-link class="link rounded-xl p-4 py-6" to="" >TRANSPORTS <br>  ROUTIERS <br> INTERURBAINS <font-awesome-icon class=" arrow" :icon="['fas', 'long-arrow-down']" /></nuxt-link>
      </div>
    </div>

    <div class="md:w-1/3 w-full h-full p-8 ">
      <div class="bg-white  h-full md:h-full w-full rounded-xl block2 relative">
          <nuxt-link class="link rounded-xl p-4 py-6" to="" >LOCATION <br> DE <br> BENNES  <font-awesome-icon class=" arrow" :icon="['fas', 'long-arrow-down']" /></nuxt-link>
      </div>
    </div>

    <div class="md:w-1/3 w-full h-full p-8 ">
      <div class="bg-white h-full md:h-full w-full rounded-xl block3 relative">
        <nuxt-link class="link rounded-xl p-4 py-6 link3" to="" > SERVICES SUR MESURE<br> ET <br> ASSISTANCE <font-awesome-icon class=" arrow" :icon="['fas', 'long-arrow-down']" /></nuxt-link>
      </div>
    </div>

  </div>
</div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
.block1, .block2, .block3{
  background-size: cover;
  transition: all 0.5s;
}
.block1{
  background-image: url('~/assets/Tesla-Guide-Semi-Hero2.jpg');
  background-position:  20%;
}
.block2{
  background-image: url('~/assets/camion_man2.png');
  background-position:  60%;
}
.block3{
  background-image: url('~/assets/fastRoad.jpg');
  background-position:  center;
}

.block1:hover{
  background-position: 30%;
}
.block2:hover{
  background-position: 70%;
}
.block3:hover{
  background-position: 60%;
}
.link{
  background-color: black;
  color:white;
  position:absolute;
  bottom:2%;
  right:5%;
  width:50%;
  font-family: 'Montserrat', sans-serif;
  font-weight:500;
  font-size:clamp(8px,0.55vw,10px);
  font-style: italic;
  letter-spacing: 2px;
  line-height:clamp(10px,0.95vw,13px);
}
.link3{
  background-color: #AE0000;
}
.arrow{
  margin-left:clamp(8px,0.55vw,12px);
  transform: scale(200%) rotate(-90deg);
  position:absolute;
  right:10%;
  margin-top: 2px;
}

@media screen and (max-width:768px){
  .link{
    bottom:10%;
    right:5%;
    width:40%;
  }
  .block2{
    background-image: url('~/assets/man_tgs_benne.png');
  }
  
}


</style>