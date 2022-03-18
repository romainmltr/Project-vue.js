<template>
    <div>
      <div class="image"></div>
      <div class="top-line"></div>

      <h1 class="title">Apprendre<br>
        VueJS</h1>

      <div class="author">

        <div class="line"></div>
        <h2>StudyCorporation</h2>
        <div class="line"></div>

      </div>
    </div>
</template>

<script>
  export default {
    data() {
      return {
        
      }
    }
  }
</script>

<style lang="scss" >
.book{
  padding: 0;
}
.image{
  position: absolute;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  z-index: -1;
  background-image: url('/src/assets/bg.png');
  background-repeat: no-repeat;
  background-size: cover;
}


.top-line {
  width: 100%;
  border: 1px solid black;
  margin-top: 50px;
}

.title {
  margin-top: 100px;
  position: relative;
  left: 33%;
  color: white;
  font-family: 'Calligraffitti', cursive;
  font-size: 40px;
  letter-spacing: 4px;
}

.author {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-top: 50%;

  .line {
    width: 100%;
    border: 1px solid black;
  }

  h2{
    padding: 1%;
    border: solid 2px black;
  }
}
</style>