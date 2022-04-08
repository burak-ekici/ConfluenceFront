<template>
  <div class=" hidden md:flex blockPrincipal">
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
  data(){
    return{
      count1: 7818,
      count2: 3120,
      count3: 1784,
      count4: 800,
    }
  },
  mounted(){
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
</script>

<style scoped>

.blockPrincipal{
  width: 100%;
  height:13vw;
  margin-top: 5vh;
}
.block{
  width:25%;
  background: #FFFCFC ;
  display:flex;
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
  justify-content: baseline;
  padding-top:25%
}

h3{
  font-family: 'Montserrat', sans-serif;
  font-style: italic;
  font-weight: 600;
  font-size:0.9vw
}
p{
  font-family: 'Montserrat', sans-serif;
  font-size:0.6vw;
  font-weight: 600;
}
.number{
  font-weight: 800;
  font-size: 1.2vw;
  margin-top:0.7vw
}
</style>