<template>
  <div class=" hidden md:flex blockPrincipal" >
    <div class="block rounded-tl-md rounded-bl-md">
      <div class="imgContainer">
        <img src="~/assets/box_icon.png" alt="eye">
      </div>
      <div class="Pcontainer">
        <h3>Fiable</h3>
        <p ref="count1" data-target="7818" class="number">0</p>
        <p>Palettes livrées</p>
      </div>
    </div>
    <div class="block">
      <div class="imgContainer">
        <img src="~/assets/dumpster_black_icon.png" alt="eye">
      </div>
      <div class="Pcontainer">
        <h3>Durable</h3>
        <p ref="count2" data-target="3120" class="number">0</p>
        <p>Bennes valorisées</p>
      </div>
    </div>
    <div class="block">
      <div class="imgContainer">
        <img src="~/assets/container_icon.png" alt="eye">
      </div>
      <div class="Pcontainer">
        <h3>Performant</h3>
        <p ref="count3" data-target="1784" class="number">0</p>
        <p>Relais achevés</p>
      </div>
    </div>
    <div class="block rounded-tr-md rounded-br-md">
      <div class="imgContainer">
        <img src="~/assets/warehouse_icon.png" alt="eye">
      </div>
      <div class="Pcontainer">
        <h3>Flexible</h3>
        <p ref="count4" data-target="800" class="number">0</p>
        <p>De stockage</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props:{
    observed:{
      type:Boolean
    }
  },
  watch:{
    observed(newValue , oldValue){
      if(newValue === true){
        this.incrementCounter()
      }
    },
    height(newValue){
      this.height = newValue
    }
  },
  methods:{
    incrementCounter(){
      const counters = [this.$refs.count1,this.$refs.count2, this.$refs.count3, this.$refs.count4]
        counters.forEach(element => {
          element.innerText = '0'
          const updateCounter = ()=>{
            const limit = +element.getAttribute('data-target')
            const increment = Math.floor(limit / 300)
            let currentValue = 0;
            const intId = setInterval(()=>{
              if(currentValue >= limit){
                clearInterval(intId)
                if(+element.getAttribute('data-target') === 800){
                  element.innerText = limit + 'm²'
                  return
                }
                element.innerText = limit
              }else{
                element.innerText = currentValue
                currentValue += increment
              }
            },1)
          }
          updateCounter()
        })
    }
  }
    
  

}
</script>

<style scoped>

.blockPrincipal{
  margin-top: 4vh;
  position:absolute;
  bottom:4vw;
  right:5%;
  left:calc(5% + 5rem );
}

.block::before{
	content: "";
	padding-bottom: 45%; 	/* initial ratio of 1:1*/
	padding-top: 45%; 	/* initial ratio of 1:1*/
}
.block{
  width:25%;
  background: #FFFCFC ;
  display:flex;
  height:100%;
  justify-content: center;
  align-items: center;
  align-content: center;
}
/* .block p:nth-child(3){
  margin-left:-2px
} */
/* .block:nth-child(1){
  border-right: 1px solid #0386FE;
}
.block:nth-child(2){
  border-right: 1px solid #0386FE;
}
.block:nth-child(3){
  border-right: 1px solid #0386FE;
} */
.block:nth-child(1){
  border-right: 1px solid black;
}
.block:nth-child(2){
  border-right: 1px solid black;
}
.block:nth-child(3){
  border-right: 1px solid black;
}
.block:nth-child(4){
  border-right: 1px solid rgba(0,0,0,0);
}
.imgContainer{
  width:50%;
  height:100%;
  display:flex;
  justify-content: center;
  align-items: center;
}

img{
  width:fit-content;
  transform: scale(0.5);
}

.Pcontainer{
  width:50%;
  height: 100%;
  display: flex;
  flex-flow:column wrap;
  padding-top:1vw;
  justify-content: center;
  align-items: flex-start;
}

h3{
  font-family: 'Montserrat', sans-serif;
  font-style: italic;
  font-weight: 600;
  font-size:clamp(10px,0.8vw,15px);
  margin-top: -2vw;
  margin-bottom: 1.3vw;
}
p{
  font-family: 'Montserrat', sans-serif;
  font-size:clamp(7px,0.6vw,12px);
  font-weight: 600;
}
.number{
  font-weight: 800;
  font-size: clamp(10px,1.4vw,20px);
}

@media screen and (min-width: 1920px){
  .blockPrincipal{
    margin-top: 8vh;
  }
  .Pcontainer{
    padding-top:0px;
  }

  h3{
    font-size:17px;
    margin-top: -30px;
  }

  p{
    font-size:12px;
  }
  .number{
    font-size:30px;
  }
}

@media only screen 
  and (min-width: 770px) 
  and (max-height: 1366px) 
  and (-webkit-min-device-pixel-ratio: 1.5) {
    
    .blockPrincipal{
      height:20vh;
      width:75%;
      display:flex;
      flex-direction: row;
      flex-wrap: wrap;
      margin:0 auto;
      bottom:30vh;
    }
    .block{
      width:50%;
      border-radius: 0%;
    }
    .block:nth-child(1){
      border-right: 1px solid black;
      border-top-left-radius: 5%;
    }
    .block:nth-child(2){
      border-right: 0px solid black;
      border-top-right-radius: 5%;
    }
    .block:nth-child(3){
      border-right: 1px solid black;
      border-bottom-left-radius: 5%;
      border-top: 1px solid black;
    }
    .block:nth-child(4){
      border-right: 0px solid rgba(0,0,0,0);
      border-bottom-right-radius: 5%;
      border-top: 1px solid black;
    }
}

</style>