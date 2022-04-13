<template>
  <div class="secondSection flex w-full md:flex-col">

      <div class="section1 relative w-1/2 flex flex-col md:h-1/2 md:w-full">

        <div class="hidden fumeeBlanc1 absolute md:block w-full h-full md:z-10"></div>

        <p class="texteBlockGauche md:relative md:z-20">TRANSPORTS ROUTIERS 
          & FRET INTERURBAINS
        </p>
        
        <div><nuxt-link to="/" class="button hidden md:block text-black absolute cursor-pointer z-20 px-4 py-3 bg-black text-white rounded">Découvrir nos offres <font-awesome-icon class="transform -rotate-90 ml-4  scale-150" :icon="['fas', 'long-arrow-down']" /></nuxt-link></div>

        <div class="flex justify-between logoArrowContainer1">

          <img class="w-1/2 md:hidden" :src="require('~/assets/container_icon.png')" alt="contour d'un container">

          <nuxt-link class="md:hidden" to="/"><font-awesome-icon class="w-1/2 arrowBlockGauche transform -rotate-90" :icon="['fas', 'arrow-down-long']" /></nuxt-link>

        </div>

      </div>

      <div class="section2 w-1/2 bg-black text-white md:h-1/2 md:w-full">

        <div class="hidden fumeeBlanc2 absolute md:block w-full h-full md:z-10"></div>

        <p class="texteBlockDroite">Location
          de
          bennes 
        </p>

        <div><nuxt-link to="/" class="button hidden md:block text-black absolute cursor-pointer z-20 px-4 py-3 bg-black text-white rounded">Découvrir nos offres <font-awesome-icon class="transform -rotate-90 ml-4  scale-150" :icon="['fas', 'long-arrow-down']" /></nuxt-link></div>

        <div class="flex justify-between logoArrowContainer2">

          <img class="w-1/2 img2 md:hidden" :src="require('~/assets/dumpster_icon.png')" alt="contour d'un container">

          <nuxt-link class="md:hidden" to="/"><font-awesome-icon class="w-1/2 arrowBlockDroite transform -rotate-90" :icon="['fas', 'arrow-down-long']" /></nuxt-link>

        </div>

      </div>

  </div>
  
</template>

<style scoped>

.secondSection{
  height: calc(25% - 8%);
  overflow: hidden;
}

.section1, .section2{
  position:relative
}

.fumeeBlanc1{
  background: linear-gradient(180deg, rgba(255,255,255,1) 0%, rgba(0,0,4,0) 52%, rgba(0,0,4,0) 100%);
}
.fumeeBlanc2{
  background: linear-gradient(0deg, rgba(255,255,255,0.7) 0%, rgba(0,0,4,0) 30%, rgba(0,0,4,0) 100%);
}

.button{
  bottom:clamp(20px,2vw,50px);
  right:clamp(20px,2vw,50px);
  text-transform: uppercase;
  font-family: 'Montserrat' , sans-serif;
  font-size: 1vw;
  font-weight:500;
  letter-spacing: 0.15vw;
}

.texteBlockGauche{
  font-family: 'Montserrat', sans-serif;
  font-weight:600;
  font-size :11px;
  font-style: italic;
  width:75%;
  padding-left:10%;
  padding-top:5%;
  letter-spacing: 1.5px;
  height:50%;
  line-height: 0.8rem;
}
.texteBlockDroite{
  font-family: 'Montserrat', sans-serif;
  font-weight:600;
  font-size :11px;
  font-style: italic;
  width:55%;
  padding-left:10%;
  padding-top:5%;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  height:50%;
  line-height: 0.8rem;
}

img{
  width:40px;
  margin: 10px 0 0 10%
}
.img2{
  color:white;
  width:40px;
  margin: 10px 0 0 10%
}

.arrowBlockGauche{
  font-size:2.5rem;
  margin-top:15px;
  margin-right:30px
}
.arrowBlockDroite{
  font-size:2.5rem;
  margin-top:15px;
  margin-right:30px
}

@media screen and (max-width: 365px){
 
  .texteBlockDroite , .texteBlockGauche{
    font-size:8px;
    line-height: 11px;
  } 

  img{
    width:30px;
    margin: 5px 0 0 10%
  }
  .img2{
    color:white;
    width:30px;
    margin: 5px 0 0 10%
  }
  .arrowBlockDroite, .arrowBlockGauche{
    transform: scale(0.5) rotate(-90deg);
  }

}
@media screen and (min-width: 366px) and (max-width : 767px){
  .texteBlockDroite , .texteBlockGauche{
    font-size:9px;
    line-height: 12px;
  } 
  .arrowBlockDroite, .arrowBlockGauche{
    transform: scale(0.75) rotate(-90deg);
    
  }
}
@media screen and (min-width: 366px) and (max-width : 767px) and (min-resolution: 190dpi){
  
  .secondSection{
    height: calc(25% - 8%);
    overflow: hidden;
  }
  img{
    padding-bottom: 2vh;
  }
  .arrowBlockDroite, .arrowBlockGauche{
    transform: scale(0.75) rotate(-90deg);
    margin-left:15vw
  }
}

@media screen and ( min-width: 769px){
  .secondSection{
    height:100%;
    width:40%;
    padding-top:4rem
  }
  .texteBlockGauche , .texteBlockDroite{
    font-size: clamp(8px,1.5vw,27px);
    line-height: clamp(11px,1.8vw,40px);
    font-weight: 700;
    width:90%;
    text-shadow: 0px 4px 4px rgba(0,0,0,0.25);
  } 
  .section1{
    background-image: url('~/assets/camion_jaune.jpg');
    background-position: 50%;
    background-size: cover;
  }
  .section2{
    background-image: url('~/assets/camion_man.jpg');
    background-position: 50%;
    background-size: cover;
    color:black
  }

  .button{
    font-size: clamp(10px, 1vw , 15px);
    letter-spacing: clamp(4px, 0.15vw , 15px);
  }
}


</style>