<template>
  <div class="Containeur h-1/2 lg:h-full flex flex-col relative lg:px-12 lg:pt-12 lg:pb-12 2xl:py-20">

    <div class="numberDiv hidden lg:block text-right font-bold"> <span class="font-bold text-3xl">01</span>/03</div>

    <div class="tripleSection">

      <div class="flex DescriptionBox items-center">
        <div class="imgContaineur">
          <img  :src="require('~/assets/container_icon.png')" alt="contour d'un contenaire" >
        </div>
        <p>Solutions de transports flexibles régionales et nationales dédiées, nous vous aidons acheminer vos matières premières et produits jusqu'a leurs destinations finales.</p>
      </div>

      <div class="flex DescriptionBox items-center">
        <div class="imgContaineur ">
          <img class="img2" :src="require('~/assets/tag.png')" alt="étiquette" >
        </div>
        <p>
          Un prix compétitif et défiant toute concurrence. Nous nous assurons de proposer une gamme de services abordables tout en augmentant la qualité de nos prestations.
        </p>
      </div>

      <div class="flex descriptionBox items-center">
        <div class="imgContaineur">
          <img :src="require('~/assets/clock.png')" alt="chronometre" >
        </div>
        <p>
          Rapidité et flexibilité, grâce à la rotation de notre personnel conducteur, nous sommes en mesure de vous proposer des solutions de transports, pour le jour même, pour pallier à vos besoins urgents.
        </p>
      </div>

    </div>

    <div class="buttonDiv flex justify-between"> 

      <nuxt-link class="w-1/2" to="/">
        <button class="buttonLeft font-semibold flex items-center">
          jE souhaite <br>
          être appeler
          <font-awesome-icon class="phone" :icon="['fa', 'phone']" />
        </button>
      </nuxt-link>

      <nuxt-link class="w-1/2 flex justify-end" to="/">
        <button class="buttonRight font-semibold flex items-center">
          je souhaite <br>
          m’informer
          <font-awesome-icon class="enveloppe" :icon="['fa', 'envelope']" />
        </button>
      </nuxt-link>

    </div>
    
  </div>
</template>


<style scoped>

.Containeur{
  width:45%;
  font-family: 'Poppins', sans-serif;
  padding-left:6rem;
}

.numberDiv{
  letter-spacing: 3px;
  margin-bottom: 8vh;
  padding-right: 7vw
}

.imgContaineur{
  width:20%;
  margin : clamp(20px,4vh,200px) 0;
  display:flex;
  justify-content: left;
}

img{
  width:40%
}

.img2{
  transform:rotate(90deg)
}

p{
  width:70%;
  font-weight:bold;
  font-size: clamp(10px,1.4vh,15px);
  letter-spacing:2px
}

.buttonDiv{
  margin-top:4vh;
  padding-right:10%;
}

.buttonLeft{
  width:95%;
  display:flex;
  justify-content:center;
  padding:0.9rem 1.6rem;
  border:3px solid #0386FE ;
  border-radius: 10px;
  color:#0386FE;
  line-height:20px;
  text-transform: uppercase;
  letter-spacing: 2px;
  font-size:clamp(9px,0.9vw,15px)
}
.buttonRight{
  width:95%;
  display:flex;
  justify-content:center;
  border:3px solid black ;
  padding:0.9rem 1.6rem;
  border-radius: 10px;
  color:white;
  background-color:black;
  line-height:20px;
  text-transform: uppercase;
  letter-spacing: 2px;
  font-size:clamp(9px,0.9vw,15px)
}



.phone{
  transform: rotate(80deg);
  font-size:1.5rem;
  margin-left: 1vw;
}

.enveloppe{
  font-size:2rem;
  margin-left: 1vw;
}

@media screen and (max-width:768px){
  
  .Containeur{
    width:100%;
    padding: 0 6vw;
  }

  .imgContaineur{
    margin : 2vh 0;
    justify-content: left;
  }

  img{
    width:60px
  }

  p{
    width:80%;
    font-weight:bold;
    font-size: 8px;
    letter-spacing:2px;
    padding-left:3vw;
    line-height: 12px;
  }
  .buttonRight{
    padding:0.4rem 0.7rem
  }

  .buttonLeft{
    padding:0.4rem 0.7rem
  }

  .phone{
    font-size:1rem;
    margin-left: 5vw;
  }

  .enveloppe{
    font-size:1.5rem;
    margin-left: 5vw;
  }

  .buttonDiv{
    margin-top:4vh;
    padding:0
  }

  
}



</style>