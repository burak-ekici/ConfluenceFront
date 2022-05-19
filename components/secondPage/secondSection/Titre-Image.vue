<template>
  <div class="Containeur">

    <!-- Version Desktop -->

    <div class="DestopContaineur hidden h-1/2 lg:h-full relative lg:pl-12 lg:pt-12 lg:pb-12 2xl:py-20 lg:flex lg:flex-row">

      <div class="w-full lg:w-1/2 relative leftContaineur">
        <h1>
          TRANSPORTS ROUTIERS <br>
          DE FRET INTERURBAINS
        </h1>
        <p class=" hidden lg:block">
          Nous fournissons des solutions de transports et logistiques adaptées à vos besoins.
        </p>
        <p class=" hidden lg:block">
          Bénéficiez de prestations sur-mesure ou partagées, à travers des prestations de relais, messagerie palettisée. 
        </p>
      </div>


      <div class="imageContainer w-full relative">
        <img class="rounded-tl-xl rounded-br-xl" :src="require('~/assets/tesla_truck_img.jpg')" alt="">
        <div class="nuageBlanc absolute w-full h-full top-0 left-0"></div>
      </div>
    
    </div>
  
    <!-- Version Mobile -->

    <div class="MobileContaineur w-full h-1/2 lg:hidden">

      <div class="TitleImageBlock">
        <div class="h1Containeur">
          <h1>
            TRANSPORTS ROUTIERS <br>
            DE FRET  <br> 
            INTERURBAINS
          </h1>
        </div>
        <div class="imageContainer w-full lg:w-1/2 h-1/2 lg:h-full relative">
          <img class="rounded-tl-xl rounded-br-xl" :src="require('~/assets/tesla_truck_img.jpg')" alt="">
          <div class="nuageBlanc absolute w-full h-full top-0 left-0"></div>
        </div>
      </div>

      <div class="pContaineurMobile">
        <p>
          Nous fournissons des solutions de transports et logistiques adaptées à vos besoins.
        </p>
        <p>
          Bénéficiez de prestations sur-mesure ou partagées, à travers des prestations de relais, messagerie palettisée. 
        </p>
      </div>
    </div>

  </div>
</template>


<style lang="scss" scoped>
.Containeur{
  width:55%
}

h1{
  font-family: 'Poppins', sans-serif;
  font-size:clamp(35px,5.5vh,55px);
  font-weight: 700;
  display:block;
  width:120%;
  letter-spacing: clamp(6.6px,1.5vh,10px);
  position:relative;
  z-index: 1;
  margin-top:30%;
}
.block{
  margin-top: 4vh;
  position:relative;
  z-index: 1;
}

p{
  font-family: 'Poppins', sans-serif;
  font-size:clamp(9px,1.2vh,12px);
  font-weight: 700;
  width:70%;
  letter-spacing:clamp(1.5px,.3vh,1.8px) ;
}
.imageContainer{
  height:100%;
}

img{
  display:block;
  height:100%;
  width:100%;
  object-fit: cover;
  object-position: 70%;
}
.leftContaineur{
  left:12%
}

.nuageBlanc{
  background:rgba(255,255,255,0.3)
}

@media screen and (max-width:1024px){
  .Containeur{
    padding:3vw;
    height:40vh;
    width:100%;
  }
}
.MobileContaineur{
  display:flex;
  flex-flow:column wrap;
  width:100vw;
  height:40vh;
  overflow:hidden;

  .TitleImageBlock{
    display: flex;
    width:100%;
    align-items: center;
    height:25vh;

    .h1Containeur{
      width:50%;
      position:relative;
      display:flex;
      align-items: center;

      h1{
        display:block;
        position:absolute;
        width:180%;
        font-size:18px;
        margin-top:0;
        line-height:29px;
        text-shadow: 0px 4px 5px rgba(0,0,0,0.3);
        left:10%;
        letter-spacing: 4px;
      }
    } 
    .imageContainer{
      width:50%;
      padding:8vw 8vw 8vw 0vw;
      img{
        width:100;
        height:100%;
        box-shadow: 0px 3px 5px rgba(0,0,0,0.4);
      }
    }
  }

  .pContaineurMobile{
    height:10vh;

    p{
      width:90%;
      display:block;
      margin:0 auto;
    }
  }
}
</style>