<template>
  <div class="containeur relative">
    <div class="logoContaineur">
      <img class="logo" src="~/assets/conf_tr_logo.png" alt="logo Confluence Transport">
    </div>
    <div class="section2">
      <p>Confluence transports, société par actions simplifiée, immatriculée sous le SIREN 838007755, est active depuis 4 années. Implantée à Lyon (69002) et à Mornant (69440), nous sommes spécialisé dans le secteur d’activité des transports routiers de fret interurbains et la livraison de bennes avec chauffeurs.</p>
        <nav class="w-full text-center text-white flex items-center justify-between lg:justify-around text-sm font-semibold">
          <NuxtLink class="hover:text-black ease-out duration-100" to='/a'>
            ACCEUIL
          </NuxtLink>
          <NuxtLink class="hover:text-black ease-out duration-100" to='/services'>
            SERVICES
          </NuxtLink>
          <NuxtLink class="hover:text-black ease-out duration-100" to='/r'>
            A PROPOS
          </NuxtLink>
          <NuxtLink class="hover:text-black ease-out duration-100" to='/z'>
            BLOG
          </NuxtLink>
        </nav>
    </div>
    <div class="section3">
      <p>Retrouvez notre actualité sur les réseaux sociaux.</p>
      <nav class="w-3/5 flex justify-between">
        <NuxtLink class="hover:text-black ease-out duration-100" to='/a'>
          <font-awesome-icon :icon="['fa-brands', 'linkedin']" />
        </NuxtLink>
        <NuxtLink class="hover:text-black ease-out duration-100" to='/v'>
          <font-awesome-icon  :icon="['fa-brands', 'facebook']" />
        </NuxtLink>
        <NuxtLink class="hover:text-black ease-out duration-100" to='/r'>
          <font-awesome-icon :icon="['fa-brands', 'facebook-messenger']" />
        </NuxtLink>
        <NuxtLink class="hover:text-black ease-out duration-100" to='/z'>
          <font-awesome-icon :icon="['fa-brands', 'snapchat-square']" />
        </NuxtLink>
      </nav>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/scss/_variables.scss';

.containeur{
  height:30%;
  position:absolute;
  bottom:0;
  right:0;
  left:0;
  background-color: $main-color;
  padding-left:6rem;
  display:flex;
  flex-flow:row nowrap;
  align-items: center;
  color:white;
 

  .logoContaineur{
    width:20%;

    .logo{
      width:80%;
    }
  }
  .section2{
    width: 45%;
    padding:2vh;

    p{
      font-family: 'Montserrat',sans-serif;
      font-weight: 500;
      font-size: clamp(11px , 1vw , 15px);
      margin-bottom:5%;
    }

    nav  a{
      text-decoration: underline;
      text-align: left;
      width:25%;
      font-family: 'Poppins', sans-serif;
      font-weight:600;
    }
  }
  .section3{
    width: 35%;
    padding:2vh;
    p{
      font-family:'Poppins', sans-serif;
      font-weight:600;
      font-size:clamp(20px,1.4vw,22px);
      margin-bottom:5%;
      text-transform: uppercase;
      letter-spacing:clamp(4px,0.3vw,7px) 
    }
    nav  a{
      text-decoration: underline;
      text-align: left;
      width:25%;
      font-family: 'Poppins', sans-serif;
      font-weight:600;
      font-size:clamp(20px,3vw,45px);

      
    }
    
  }
  @media screen and (max-width:1400px) and (min-resolution: 190dpi){
      .logoContaineur{
        display:none
      }
      .section2{
        display:none
      }
      .section3{
        width:100%;
        margin-top:-3vh;
        p{
          text-align: center;
        }
        nav{
          justify-content: space-between;
          width:100%;

          a{
            transform: scale(200%);
            transform-origin: center;
            text-align: center;
          }
        }
      }
  }
  @media screen and (max-width:768px){
    .logoContaineur{
        display:none
      }
      .section2{
        display:none
      }
      .section3{
        width:100%;
        margin-top:-3vh;
        p{
          text-align: center;
        }
        nav{
          justify-content: space-between;
          width:100%;

          a{
            transform: scale(200%);
            transform-origin: center;
            text-align: center;
          }
        }
      }
  }
  @media screen and (max-width:1400px) and (min-resolution: 190dpi){
    .section3{
      transform: scale(70%);
      margin-top:-5vh;

      p{
        margin-bottom:5vh;
      }
    }
  }
}
@media screen and (max-width:1400px) and (min-resolution: 190dpi){
  .containeur{
    padding-left: 0;
  }
}
@media screen and (max-width:768px){
  .containeur{
    padding-left: 0;
  }
}

</style>