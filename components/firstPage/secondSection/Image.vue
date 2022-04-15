<template>
  <div class=" h-full w-full relative">
    <div class="md:block md:absolute md:top-0 md:bottom-0 md:right-0 md:left-0 fumeeNoir z-10"></div>
    <div class="absolute z-20 Pcontainer">
      <p class="w-full"><img :src="require('~/assets/container_white_icon.png')" alt=""> <span ref="countImgSection2" data-target="1784" class="number text-3xl ml-4 relative top-2">1784</span> </p>
      <p class="w-full mt-2">Relais terminées</p>
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
    }
  },
  methods:{
    incrementCounter(){
      const counters = [this.$refs.countImgSection2]
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
.fumeeNoir{
  background: linear-gradient(0deg, rgba(0,0,0,0.7) 0%, rgba(0,0,4,0) 30%, rgba(0,0,4,0) 100%);
}

img{
  width:40px;
  display: inline-block;
}
p{
  font-family: 'Montserrat', sans-serif;
}
p:nth-child(1){
  text-align: right;
}
p:nth-child(2){
  font-family: 'Poppins', sans-serif;
  font-size: 2vw;
}
.Pcontainer{
  bottom:6vw;
  right:4vw
}
.number{
  font-weight: 600;
}

@media screen and (max-width : 768px){
  .number{
    font-size: clamp(27px,9vw,45px);
  }
  img{
    width:40px;
    display: inline-block;
  }
  p:nth-child(1){
    text-align: left;
  }
  p:nth-child(2){
    font-size: clamp(20px,8vw,35px);
    font-weight: 500;
  }
  
  .Pcontainer{
    top:10%;
    left:4vw
  }
  .fumeeNoir{
    display:block;
    background: linear-gradient(0deg, rgba(0,0,0,0.4) 0%, rgba(0,0,4,0.4) 100%);
    width:100%;
    height:100%
  }
}

@media screen and (min-width : 800px) and (max-width : 1367px) and (min-resolution : 190dpi){
  .Pcontainer{
    bottom:8vw;
    right:8vw
  }
}

</style>