<template >
  <i class="fa-solid fa-chevron-left arrow arrow_left" @click="decrement"></i>
  <div class="book">
    <Page1 v-if="count === 1"></Page1>
    <Page2 v-else-if="count === 2"></Page2>
    <Page3 v-else-if="count === 3"></Page3>
    <Page4 v-else-if="count === 4"></Page4>
    <Page5 v-else-if="count === 5"></Page5>
    <Page6 v-else-if="count === 6"></Page6>
    <Page7 v-else-if="count === 7"></Page7>
  </div>
  <i class="fa-solid fa-chevron-right arrow arrow_right" @click="increment"></i>
  <input type="number" v-model="count" name="count" id="" min="1" max="6" class="selectPage">
</template>

<script>
import PageAccueil from "./components/PageAccueil.vue"
import Page5 from './components/Page5.vue';
import Histoire from './components/Histoire.vue'
import Installation from './components/Installation.vue'
import Syntaxe from './components/Syntaxe.vue'
import Sommaire from './components/Sommaire.vue'
import Exemples from './components/Page7.vue'

export default {
  name: 'App',
  components:{
    'Page1': PageAccueil,
    'Page2': Sommaire,
    'Page3': Histoire,
    'Page4': Installation,
    'Page5': Page5,
    'Page6': Syntaxe,
    'Page7': Exemples
  },
  data () {
    return {
      count: 1
    }
  },
  methods:{
    increment() {
      this.count = this.count === 7 ? 7 : this.count + 1;
    },
    decrement() {
      this.count = this.count === 1 ? 1 : this.count - 1;
    }
  }
}

</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&display=swap');
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: 'Open Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 100vh;
  align-items: center;
  display: flex;
  justify-content: space-between;
}

.arrow{
  font-size: 40px;
  cursor: pointer;
}

.arrow_left{
  margin-left: 50px;
}

.arrow_right{
  margin-right: 50px;
}

.book{
  width: 30%;
  height: 80%;
  position: relative;
  padding: 30px;
  box-shadow: 0 4px 8px rgba($color: #000000, $alpha: 0.2);
}

.selectPage{
  position: absolute;
  left: 50%;
  bottom: 10px;
  transform: translate(-50%, -50%);
  padding: 5px 10px;
}

</style>