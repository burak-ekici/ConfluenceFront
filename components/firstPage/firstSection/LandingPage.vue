<template>
  <div ref="landingPage" id="first" class="relative containeur w-full h-screen absolute top-0 bottom-0 md:flex">

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

        <FirstPageFirstSectionWhiteBlock :observed="observerIsActivatedComputed" />

      </div>

    </div>

    <FirstPageFirstSectionSecondSection />

    <FaireDefiler hashToScrollBottom="second" hashToScrollTop="" />

  </div>
</template>

<script>
export default{
    data(){
      return{
        observerIsActivated : false
      }
    },
    computed: {
      observerIsActivatedComputed(){
        return this.observerIsActivated
      }
    },
    mounted(){
      const options = {
        root: null,
        rootMargin: '0px',
        threshold:0.2
      }
      const observer = new IntersectionObserver((entries , observer)=>{
        entries.forEach( entry => {
          if(entry.isIntersecting){
            this.observerIsActivated = true
          }
        })
        
      }, options);

      observer.observe(this.$refs.landingPage)
    }
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
  line-height: 1.2vw;
}

.PremierP{
  font-family: 'Montserrat', sans-serif;
  font-size:20px;
  font-weight:bold;
  letter-spacing: 4px;
  line-height: 30px;
}

.SecondP, .TroisiemeP{
  font-family: 'Montserrat', sans-serif;
  font-size:14px;
  font-weight:500;
  line-height: 0.75vw;
  line-height: 20px;
}
.button{
  border-width: 2px;
  font-size:12px;
  font-family: 'Montserrat', sans-serif;
  font-weight:bold;
}
.arrow{
  top: 2px;
  left:20px;
}



@media screen and (max-width: 365px){
  .PremierP{
  font-size:14px;
  letter-spacing: 3px;
  margin-top: -10px
}
  .button{
    margin-top:10px;
    padding:10px 20px;
    font-size: 9px;
  }
  .SecondP, .TroisiemeP{
    font-size:10px;
    line-height: 20px;
    margin-top:20px
  }
  .arrow{
    left:3px;
    top:0px
  }

}

@media screen and (min-width:366px) and (max-width: 464px){
  .button{
    margin-top:0px
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
    font-size:2vh;
    line-height: 3vh;
    margin-top:4%;
  }

  .buttonDiv{
    margin-top:15%
  }
}

@media screen and (min-width: 769px){
  .principal{
    height:100%;
    width:60%;
  }
  .insidePrincipal{
    padding:10% 5% 0% calc(5% + 5rem) ;
  }
  .PremierP{
    font-size:clamp(15px,2vw,25px);
    line-height: clamp(20px,2.5vw,35px);
    margin-top:11%;
    margin-bottom: 20px;
  }

  .SecondP, .TroisiemeP{
    font-size:clamp(13px,2.5vw,17px);;
    font-weight: 500;
    line-height: clamp(18px,3vw,25px);
    margin-top:30px
  }


  .buttonDiv{
    margin-top:5%;
    justify-content: flex-start;
  }
  .button{
    padding:1.5vh 4vh;
    font-size:0.75vw;
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

@media screen and (min-height: 900px) and (min-width : 1700px){
  .PremierP{
    font-size : 25px;
  }
  .SecondP, .TroisiemeP{
    font-size:17px;
    margin-top:20px
  }
}

@media screen and (min-height: 1400px){
  .PremierP{
    margin-top: 200px;
  }
  .SecondP, .TroisiemeP{
    margin-top:50px
  }
}

@media only screen and ( min-resolution: 190dpi) and (max-width: 464px){
  
  .insidePrincipal{
    padding-top : 100px;
  }
  .PremierP{
    font-size: 2vh;
    line-height: 3vh;
  }
  .SecondP,.TroisiemeP{
    font-size : 1.6vh;
    margin-top: 3vh;
  }
  .button{
    font-size: 10px;
  }
  .buttonDiv{
    margin-top:20px
  }
  
}

</style>