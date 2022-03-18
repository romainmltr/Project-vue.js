<template>
<section>
    <div class="border"></div>
    <p class="numberPage">5</p>
    <h1>Evènements</h1>
    <h2>Écouter des évènements</h2>
    <p>Nous pouvons intercepter un événement en ajoutant la <span>v-on</span> directive à l'élément DOM concerné. Disons que nous voulons gérer un clic sur un élément de bouton
    - nous pouvons ajouter ce qui suit à notre modèle Vue:</p>
    <p>Il est possible pour v-on d'accepter le nom d’une méthode que vous voudriez appeler, lors d'un évènement plus complexe.</p>
    <h2>Modificateurs d’évènements</h2>
    <p>Il est courant de faire appel à <span>event.preventDefault()</span> ou <span>event.stopPropagation()</span> . Pour faciliter la chose,
    Vue propose des modificateurs d’évènements pour <span>v-on</span> tels que : </p>
    <ul>
        <li>.stop</li>
        <li>.prevent</li>
        <li>.capture</li>
        <li>.self</li>
        <li>.once</li>
        <li>.passive</li>
    </ul>
</section>
</template>


<script>
export default {
  name: 'Mama_'
}

</script>



<style lang="scss" scoped>



section{

    .numberPage{
      position: absolute;
      bottom: 10px;
      right: 20px;
      color: #3fb984;
      font-weight: normal;
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
    p{
        font-weight: 600;
        font-size: 16px;
    }
            
    span {
        color: #31475e;
        font-weight: 700;
    }
    h2{
    color: #f25417;
    font-size: 20px;
    margin: 10px 0;
    }
        
    ul{
        width: fit-content;
        margin: 0 auto;
        li{
            list-style-type: disc;
            font-weight: 600;

            &::marker{
                color: #3fb984;
            }
        }   
    }
}
</style>
