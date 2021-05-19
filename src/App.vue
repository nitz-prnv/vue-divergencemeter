<template>
  <div id="app">
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link
      href="https://fonts.googleapis.com/css2?family=Nixie+One&display=swap"
      rel="stylesheet"
    />
    
    <div @click="SetDivergence" id="display" v-if="divergence">
      <div v-for="value in divergence" v-bind:key="value" id="number">
        <div>{{ value }}</div>
      </div>
    </div>
    <!-- <img src="https://fanart.tv/api/download.php?type=download&image=40282&section=1" alt=""> -->
    <UnderConstruction/>
  </div>
</template>

<script>
import UnderConstruction from './components/UnderConstruction'
export default {
  name: "App",

  components: {UnderConstruction},

  data() {
    return {
      divergence: '1.048596',
    };
  },
  methods: {
    SetDivergence() {
      let StrDiv = "0.328403";
      this.divergence = StrDiv.split("");
    },
  },
};
</script>

<style >
#display {
  display: flex;
  flex-direction: row;
  justify-content: center;
  /* align-self: center; */
  color: rgb(253, 178, 124);
  background-color: rgb(27, 23, 23);
  text-shadow: 1px 1px 2px rgb(235, 90, 53), 0 0 20px rgb(255, 60, 0),0 0 8px rgb(139, 9, 0);
  text-align: center;
  font-size: 9vw;
  position: relative;
  width: auto;
  border: 2vw double rgb(196, 193, 188);
  border-radius: 3vw 3vw 0px 0px;
  border-bottom:1vw double rgb(196, 193, 188) ;
  border-top:1vw solid rgb(196, 193, 188) ;
  font-family: "Nixie One", cursive;
}
#number {
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
  padding: 1%;
  margin-top: 1%;
  margin-left: 1% ;
  margin-right: 1% ;
  width:7%;
  border: 2px solid wheat;
  background-color: rgba(56, 26, 26, 0.575);
  border-radius: 2vw 2vw 0px 0px;
  
}
#app{
  padding: 1%;
  display: flex;
  flex-direction: column;
  
}
html{
  background-color: black;
}

</style>
