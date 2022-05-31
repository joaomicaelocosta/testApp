<template>
  <div id="app">
    <h1>Answer this questions to know if you are gay!</h1>
    <h2>{{question}}</h2>
    <div class="button-div" v-if="!isFinal">
      <div class="but" @mouseover="first = 'Hell Yeah!', second = 'No!'" @click="next">{{first}}</div>
      <div class="but" @mouseover="second = 'Hell Yeah!', first = 'No!'" @click="next">{{second}}</div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      first: 'Hell Yeah!',
      second: 'No!',
      question:'Are you gay?',
      state:0,
      isFinal: false,
    }
  },
  methods: {
    next() {
      this.state++;
      switch(this.state) {
        case 1:
          this.question = "Do you like to get your ass fucked?";
          break;
        case 2:
          this.question = "Do you enjoy being dominated by men?";
          break;
        case 3:
          this.question = "Do you like to have cum deep inside your ass?";
          break;
        case 4:
          this.question = "Do you enjoy gargling semen?";
          break;
        case 5:
          this.isFinal = true;
          this.question = "Congratulations you are gay!"
          break;
      }

      
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.button-div{
  max-width: 300px;
  margin: auto;
  display: flex;
  justify-content: space-between;
  gap: 10px;
}
.but{
  flex:1;
  padding: 0.5rem 2rem;
  border-radius: 7px;
  background-color: #2c3e50;
  color: #fff;
  cursor: pointer;
}
</style>
