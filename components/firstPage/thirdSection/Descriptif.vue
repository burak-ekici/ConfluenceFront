<template>
  <div class="containeur bg-white w-full h-full">

    <div class="Titre_Paragraphe">
      <h2>LOCATION DE BENNES AVEC CHAUFFEUR </h2>
      <h3>Evacuations et traitements des déchets sans minimum de poids imposé.</h3>
      <p>Nous intervenons aux alentours de Corbas et Mornant sur un rayon de 20km. Nous assurons la pose et le retrait de la benne en un temps record. Par le biais de notre démarche environnementale nous limitons l’impact environnemental de vos activités, en prenant soin de valoriser vos déchets et de les inscrire dans un cadre de développement durable. </p>
    </div>

    <div class="Qualite">
      <div>
        <span><font-awesome-icon class="text-white" :icon="['fas', 'check']" /></span> <p>Vous ne payez que le poids de ce que vous jetez.</p>
      </div>
      <div>
        <span><font-awesome-icon class="text-white" :icon="['fas', 'check']" /></span> <p>Tarification unique, quelque soit la dimension de la benne.</p>
      </div>
      <div>
        <span><font-awesome-icon class="text-white" :icon="['fas', 'check']" /></span> <p>Tarification unique pour les périodes allant de 1 à 7 jours. </p>
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
      align-items: center;
      span{
        display:flex;
        justify-content: center;
        align-items: center;
        background:#0386FE;
        padding:4px;
        border-radius: 50%;
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
        margin-left: 5%;
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

      &:hover{
        background:black;
        color:white;
      }
      .arrow{
        margin-left: 2vw;
        padding-right: 4px;
      }
    }
    
  }
}



@media screen and (max-width : 768px){
  .containeur{
    

    .Titre_Paragraphe{
      padding-top: 3vh;

      h2{
        margin-bottom: 0.75vh;
      }
      p{
        margin-top:1.5vh;
      }
    }
    .Qualite{
      margin-top:4vh;
      width:100%;

      div{
        margin-bottom: 2vh;
      }
    }

    .Confiance{
      margin-top: 3vh;
      .LOGO{
        img{
          width:50%;
          transform: scale(80%);
        }
      }
    }

    .buttonDiv{
      position:absolute;
      bottom:2vh;
      right:10%;
      z-index:20;
      
      
      a{
        background:black;
        color:white;
        padding: 2vh 4vw;

        &:hover{
          background:black;
          color:white;
        }
  
      }
      
    }
  }
}



@media screen and (min-width : 768px){
  .buttonDiv{
      float:right;
      margin-bottom:2vh;

      a{
        width:auto;
        text-align: center;
      }
  }
  

}

@media screen and (max-width : 390px) and (min-resolution : 190dpi){
  .containeur{
    transform: scale(0.8);
    margin-top:-4vh;

    .buttonDiv{
      bottom: -3vh;
    }

  } 
  
}





</style>