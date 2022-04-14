<template>
  <div class="containeur bg-white w-full h-full">

    <div class="Titre_Paragraphe">
      <h2>TRANSPORTS ROUTIERS DE FRET INTERURBAINS</h2>
      <h3>Fournir une gamme complète de transport à l'échelle nationale.</h3>
      <p>Opérateur logistique représentatif offrant une gamme complète de services dans le domaine du transports et de la location de bennes en région lyonnaise.</p>
      <p>Nous intervenons périodiquement auprès d’associations de transports européennes pour des opérations d’assistances et de logistiques du dernier kilomètre.</p>
    </div>

    <div class="Qualite">
      <div>
        <span></span> <h4>Qualité</h4> <p>Nous misons sur l’entière satisfaction de nos prestataires à travers notre organisation et nos prestations.</p>
      </div>
      <div>
        <span></span> <h4>Assistance</h4> <p>Nos équipes sont toujours mobilisées pour des prestations d’assistances et de relais.</p>
      </div>
    </div>

    <div class="Confiance">
      <h3>Ils nous font confiance</h3>
      <div class="LOGO">
        <img src="@/assets/fnac_darty_rect.png" alt="logo fnac darty">
        <img src="@/assets/breger_rect.png" alt="logo breger">
        <img src="@/assets/xpo_rect.png" alt="logo xpo">
      </div>
    </div>

    <div class="buttonDiv">
      <nuxt-link class="flex items-center" to="">En savoir plus <font-awesome-icon class="transform scale-125 -rotate-90 arrow" :icon="['fas', 'long-arrow-down']" /></nuxt-link>
    </div>
    
  </div>
</template>

<style lang="scss" scoped>
.containeur{
  padding:5%;
  position:relative;
  .Titre_Paragraphe{
    font-family: 'Poppins',sans-serif;
    padding-top: 12vh;

    h2{
      font-size:clamp(20px,1.4vw,24px);
      font-weight: 900;
      letter-spacing: 0.3vw;
      margin-bottom: 1.5vh;
    }
    h3{
      color:#0386FE;
      font-weight: 600;
      font-size: clamp(14px,1.05vw,18px);
      letter-spacing: 0.1vw;
    }
    p{
      font-family: 'Montserrat', sans-serif;
      margin-top:3vh;
      font-weight: 500;
      font-size: clamp(11px,0.8vw,14px);
    }
  }

  .Qualite{
    margin-top:5vh;
    width:100%;

    div{
      display:flex;
      align-items: baseline;
      font-family: 'Poppins',sans-serif;
      margin-bottom: 3vh;
      span{
        display:block;
        background:#0386FE;
        width:10px;
        height:10px;
        border-radius: 2px;
      }
      h4{
        font-size: clamp(11px,0.8vw,14px);
        font-weight: 600;
        display:block;
        width:30%;
        padding-left: 3vw;
      }
      p{
        display: block;
        width:calc(70% - 10px);
        font-weight: 400;
        font-size: clamp(11px,0.8vw,14px);
      }
    }
  }

  .Confiance{
    font-family: 'Poppins',sans-serif;
    margin-top: 6vh;
    h3{
      font-size: clamp(11px,0.8vw,14px);
      font-weight: 600;
    }
    .LOGO{
      display:flex;
      flex-flow:row wrap;
      justify-content: center;
      img{
        width:50%;
      }
    }
  }

  .buttonDiv{
    position:absolute;
    bottom:5vh;
    right:5vh;
    
    a{
      font-size: clamp(11px,0.95vw,15px);
      border:2px solid black;
      border-radius: 3px;
      padding:1.5vh 2vw;
      font-family: 'Montserrat', sans-serif;
      font-weight: 700;
      .arrow{
      margin-left: 2vw;
      padding-right: 4px;
    }
    }
    
  }
}



</style>