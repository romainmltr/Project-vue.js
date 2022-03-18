<template>

<section class='test'>
<p> lorem ipsum dolor sit amet, consectetur <span>aez,kaz,eaz</span>adipiscing elit et just aliquet et just al 
</p>
<img src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/langfr-220px-Vue.js_Logo_2.svg.png'>
</section>
</template>


<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style lang="scss" scoped>
p{
    color:red;
    span{
        color:green;
    }
}

</style>
