<template>
  <div class="containeur">
    <h2>CHEZ CONFLUENCE TRANSPORTS
        <span> ça ARRIVE TOUJOURS à bon port.</span> 
    </h2>
  </div>
</template>

<style lang="scss" scoped>
.containeur{
  height:70%;
  width:100%;
  background: url('~/assets/Tesla-Guide-Semi-Hero.jpg');
  background-position:center;
  background-size: cover;
  display:flex;
  justify-content: center;
}
h2{
  text-transform: uppercase;
  font-family: 'Poppins', sans-serif;
  font-weight:700;
  color:black;
  margin-top:10vh;
  font-size: clamp(27px, 2vw, 45px);
  width:50%;
  text-align: center;
  letter-spacing: clamp(3px, 0.3vw, 7px);
  span{
    width:100%;
    display:block;
  }
}

@media screen and (max-width:768px){
  h2{
    width:90%
  }
}

@media screen and (min-width : 800px) and (max-width : 1367px) and (min-resolution : 190dpi){
  h2{
    width:70%
  }
}
</style>