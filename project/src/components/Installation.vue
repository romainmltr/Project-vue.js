<template>
    <div>
        <div class="border"></div>
        <p>4</p>
        <h1>Installation</h1>
        <div class="content">
            <ul>
                <li>
                    Pre-requis
                    <ul>
                        <li>Node.js sur votre machine</li>
                    </ul>
                </li>
                <li>
                    Commande a éffectué pour l'installation.
                    <ul>
                        <li>>npm init vue@latest</li>
                        <li>> cd your-project-name</li>
                        <li>> npm install</li>
                        <li>> npm run serve</li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Installation_',
}
</script>

<style lang="scss" scoped>


        p{
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
                border-radius: 25px;
            }
        }

        .content{
            margin-left: 40px;
            height: 80%;

            ul{
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                height: 100%;
            }

            li{
                color: #31475e;
                margin: 25px 0 0;
                font-size: 24px;
                font-weight: 600;

                span {
                    color: #3a699b;

                    a {
                        color: #3a699b;
                    }

                    a:hover {
                        color: darken($color: #3a699b, $amount: 20);
                    }
                }

                ul {
                    margin-left: 25px;
                }

            &::marker{
                color: #3fb984;
                }
            }
        }

    .none {
        display: none;
    }

</style>