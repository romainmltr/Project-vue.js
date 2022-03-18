<template>
    <div class="examples">
        <div class="border"></div>
        <h1>Exemples d'utilisation</h1>
        <p class="numberPage">7</p>
        <h2>v-model</h2>
        <div class="image_example">
          <label for="image">Image :</label>
          <input type="text"  v-model="image" placeholder="Insere le lien d'une image" class="insertImage" name="image">  
        </div>
        <div class="image_v_model">
          <img :src="image" alt="" >
        </div>
        <div>
          <label for="color">Color :</label>
          
          <input v-model="color" type="color">
        </div>
        <p :style="{'color' : color}" class="colors">Message is: {{ color }}</p>

        <h2>v-if / v-else</h2>
        <div class="pair_impair">
          <button @click="random">Click</button>
          <h2>{{number}}</h2>
          <h3 v-if="number % 2">Nombre Impair</h3>
          <h3 v-else>Nombre Pair</h3>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Exemple_',

  data(){
    return{
        image: '',
        color: '',
        number: 0,
    }
  },
  methods:{
    random(){
      this.number = Math.ceil(Math.random()*1000)
    }
  }
}

</script>

<style lang="scss" scoped>

    .numberPage{
      position: absolute;
      bottom: 10px;
      right: 20px;
      color: #3fb984;
    }

    .border{
      position: absolute;
      left: 0;
      z-index: 10;
      top: 0;
      height: 100%;
      background-color: #31475e;
      width: 3%;
    }

    .examples{
      input{
        border: none;
        margin-left: 10px;
        background: none;
      }
    }

    h1{
      text-align: center;
      font-size: 40px;
      color:  #31475e;
      position: relative;
      width: auto;
      
      &:after{
        content: "";
        position: absolute;
        left: 50%;
        transform: translate(-50%, -50%);
        bottom: 5px;
        width: 20%;
        background-color: #3fb984;
        height: 3px;
        border-radius: 50px;
      }
    }

    h2{
        color: #f25417;
        font-size: 20px;
        margin: 10px 0;
    }

    label, p{
      font-weight: 600;
    }

    .colors{
      padding-bottom: 5px;
      border-bottom: 1px solid #000;
    }

    .insertImage{
      padding: 5px 10px;
      border: none;
      border-bottom: 1px solid black;
    }

    .image_v_model{
      margin-top: 10px;
      height: 100px;
    }

    .image_v_model img{
      width: 100%;
      max-height: 100px;
      object-fit: contain;
      object-position: center;
    }

    button{
      background-color: none;
      border: none;
      background: none;
      cursor: pointer;
      border-bottom: 1px solid #3fb984;;
    }
</style>