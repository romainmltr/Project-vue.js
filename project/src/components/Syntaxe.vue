<template>
    <section>
        <div class="border"></div>
        <p class="numberPage">6</p>
        <h2>Syntaxe</h2>
        <div class="pres">
            <p>Vue.js utilise une syntaxe de template basée sur le HTML qui vous permet de lier déclarativement le DOM
                rendu aux données de l’instance sous-jacente de Vue. Tous les templates de Vue.js sont du HTML valide
                qui peut être interprété par les navigateurs et les interpréteurs HTML conformes aux spécifications.</p>

        </div>

        <div class="synt">
            <pre><code class="language-html">
&lt;template>
&lt;div class="hello">
    &lt;h1> { {title} }  &lt;/h1>
&lt;/div>
&lt;/template>


&lt;script>
    export default {
        name: 'app',
        data() {
            return {
                title: 'Hello World'
            };
        },
    };
&lt;/script>

&lt;style>

&lt;/style>
</code></pre>
</div>


</section>
</template>


<script>
    import Prism from "prismjs";
    import "prismjs/themes/prism.css"; // you can change
    export default {
        name: 'app',
        data() {
            return {
                //
            };
        },
        // mounted
        mounted() {
            window.Prism = window.Prism || {};
            window.Prism.manual = true;
            Prism.highlightAll(); // highlight your code on mount
        }
    };
</script>

<style scoped lang="scss">
    section {
        h2{
            text-align: center;
            font-size: 40px;
            color:  #31475e;
            position: relative;

            &:after{
                content: "";
                position: absolute;
                left: 50%;
                transform: translate(-50%, -50%);
                bottom: 10px;
                width: 20%;
                background-color: #3fb984;
                height: 3px;
                border-radius: 50px;
            }
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

        .numberPage{
            position: absolute;
            bottom: 10px;
            right: 20px;
            color: #3fb984;
        }

        .pres p {
            font-size: 16px;
            font-weight: 600;
        }

        .synt{
            font-size: 8px;
        }
    }
</style>