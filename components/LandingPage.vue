<template>
  <div class="relative h-screen absolute top-0 bottom-0">

    <div class="principal relative">

      <div class="insidePrincipal h-full w-full absolute top-0 left-0 bottom-0 right-0 text-black pt-24 px-8 md:pt-24 md:pl-24">

        <p class="block PremierP mt-4">
          TRANSPORTS ROUTIERS DE FRET INTERURBAINS
          ET LOCATIONS DE BENNES
        </p>

        <p class="mt-10 SecondP">
          Opérateur logistique représentatif offrant une gamme complète de services dans le domaine du transports et de la location de bennes en région lyonnaise.
        </p>

        <p class="mt-6 TroisiemeP">
          Nous intervenons périodiquement auprès d’associations de transports européennes pour des opérations d’assistances et de logistiques du dernier kilomètre.
        </p>

        <div class="w-full flex justify-between mt-12 buttonDiv">

          <button class="button border border-black px-6 sm:px-10 py-3 rounded">En savoir plus</button>
          <button class="button border border-black pl-3 pr-9 sm:pl-6 sm:pr-14 py-3 text-left rounded text-white bg-black relative">Nos services <font-awesome-icon class="transform -rotate-90 text-white scale-150 relative arrow" :icon="['fas', 'arrow-down']" /></button>

        </div>

        <WhiteBlockFirstSection />

      </div>

    </div>

    <div class="secondSection flex w-full">
      <div class="section1 w-1/2 flex flex-col">
        <p class="texteBlockGauche">TRANSPORTS ROUTIERS 
          & FRET INTERURBAINS
        </p>
        <div class="flex justify-between">
          <img class="w-1/2" :src="require('~/assets/container_icon.png')" alt="contour d'un container">
          <nuxt-link to="/"><font-awesome-icon class="w-1/2 arrowBlockGauche transform -rotate-90" :icon="['fas', 'arrow-down-long']" /></nuxt-link>
        </div>
      </div>
      <div class="section2 w-1/2 bg-black text-white">
        <p class="texteBlockDroite">Location
          de
          bennes 
        </p>
        <div class="flex justify-between">
          <img class="w-1/2 img2" :src="require('~/assets/dumpster_icon.png')" alt="contour d'un container">
          <nuxt-link to="/"><font-awesome-icon class="w-1/2 arrowBlockDroite transform -rotate-90" :icon="['fas', 'arrow-down-long']" /></nuxt-link>
        </div>
      </div>
    </div>

    <FaireDefilerBottom hashToScroll="#" />

  </div>
</template>

<script>
import WhiteBlockFirstSection from "./firstPage/WhiteBlockFirstSection.vue";
export default{
    components: { WhiteBlockFirstSection }
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,500;1,200;1,500&display=swap');
.principal{
  height:75%;
  background: url('~/assets/tesla_truck_img.jpg');
  background-size:cover;
  background-position: 60% top ;
}
.insidePrincipal{
  background: rgba(255,255,255,0.5);
  line-height: 1.6rem;
}

.PremierP{
  font-family: 'Montserrat', sans-serif;
  font-size:24px;
  font-weight:bold;
  letter-spacing: 4px;
}

.SecondP, .TroisiemeP{
  font-family: 'Montserrat', sans-serif;
  font-size:14px;
  font-weight:500;
  line-height: 1rem;
}
.button{
  border-width: 2px;
  font-size:12px;
  font-family: 'Montserrat', sans-seri8;;
  font-weight:bold
}

.arrow{
  top: 2px;
  left:20px;
}

.secondSection{
  height: calc(25% - 8%)
}

.section1, .section2{
  position:relative
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
  .PremierP{
  font-size:20px;
  letter-spacing: 3px;
  margin-top: -10px
}
  .button{
    padding:5px 15px;
    margin-top:20px;
    padding:5px 11px;
    font-size: 9px;
  }
  .SecondP, .TroisiemeP{
  font-size:14px;
  line-height: 0.9rem;
  margin-top:40px
}
  .arrow{
    left:3px;
    top:0px
  }

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

}

@media screen and (min-width:366px) and (max-width: 464px){
  .button{
    margin-top:60px
  }
}

@media screen and (min-width: 464px) and (max-width:768px){
  .insidePrincipal{
    padding:110px 10% 0% 10%;
    
  }
  .PremierP{
    margin-top:0px
  }

  .SecondP, .TroisiemeP{
    font-size:17px;
    line-height: 1.3rem;
    margin-top:9%;
  }

  .buttonDiv{
    margin-top:15%
  }
}

@media screen and (min-width: 769px){
  .principal{
    height:100%;
    width:65%;
  }
  .insidePrincipal{
    padding:20% 5% 0% calc(5% + 4rem) ;
  }
  .PremierP{
    font-size:2vw;
    line-height: 2.2rem;
    margin-top:11%
  }

  .SecondP, .TroisiemeP{
    font-size:1.4vw;
    font-weight: 500;
    line-height: 1.8rem;
  }
  .TroisiemeP{
    margin-top:0
  }

  .buttonDiv{
    margin-top:5%;
    justify-content: flex-start;
  }
  .button{
    padding:1.5vh 4vh;
    font-size:1vw;
  }
  .arrow{
    top:0
  }

  .button:nth-child(1){
    transform-origin: left;
  }

  .button:nth-child(2){
    transform-origin: right;
    margin-left:1vw;
  }
}



</style>