<script>
    export default {
        data() {
            return {
                cardsLeft: [
                    {
                        icon: '💡',
                        functionTitle: 'Instant Server Start',
                        description: 'On demand file serving over native ESM, no bundling required!'
                    },
                    {
                        icon: '⚡️',
                        functionTitle: 'Lightning Fast HMR',
                        description: 'Hot Module Replacement (HMR) that stays fast regardless of app size.'
                    },
                    {
                        icon: '🛠️',
                        functionTitle: 'Rich Features',
                        description: 'Out-of-the-box support for TypeScript, JSX, CSS and more.'
                    }
                ],
                cardsRight: [
                    {
                        icon: '📦',
                        functionTitle: 'Optimized Build',
                        description: 'Pre-configured Rollup build with multi-page and library mode support.'
                    },
                    {
                        icon: '🔩',
                        functionTitle: 'Universal Plugins',
                        description: 'Rollup-superset plugin interface shared between dev and build.'
                    },
                    {
                        icon: '🔑',
                        functionTitle: 'Fully Typed APIs',
                        description: 'Flexible programmatic APIs with full TypeScript typing.'
                    }
                ],
            }
        }
    }
</script>

<template>
    <div class="jumbotron-container">
        <!-- Left side -->
        <div class="jumbotron-container__left">
            <div class="card" v-for="card in cardsLeft">
                <div class="card__icon">
                    <span>{{card.icon}}</span>
                </div>
                <div class="card__title">
                    <h3>{{card.functionTitle}}</h3>
                </div>
                <div class="card__description">
                    <p>{{card.description}}</p>
                </div>
            </div>
        </div>
        <!-- /Left side -->

        <!-- Middle side -->
        <div class="jumbotron-container__middle">
            <div class="image-bg"></div>
            <img src="https://vitejs.dev/logo-with-shadow.png" alt="logoViteJs">
            <div class="title">
                <h1>Vite ~ Next Generation Frontend Tooling</h1>
            </div>
        </div>
        <!-- /Middle side -->

        <!-- Right side -->
        <div class="jumbotron-container__right">
            <div class="card" v-for="card in cardsRight">
                <div class="card__icon">
                    <span>{{card.icon}}</span>
                </div>
                <div class="card__title">
                    <h3>{{card.functionTitle}}</h3>
                </div>
                <div class="card__description">
                    <p>{{card.description}}</p>
                </div>
            </div>
        </div>
        <!-- /Right side -->
    </div>
</template>

<style scoped>
    /*------------------
        JUMBOTRON STYLE
    -------------------*/
    .jumbotron-container{
        background-color: #242424;
        display: flex;
        color: white;
    }
    .jumbotron-container__left {
        width: 30%;
    }
    .jumbotron-container__middle{
        width: 40%;
        display: flex;    
        justify-content: center;
        align-items: center;
        padding: 5rem 3.125rem;
    }
    .jumbotron-container__middle .image-bg{
        background-image: linear-gradient( -45deg, #bd34fe 50%, #47caff 50%);
        filter: blur(4.5rem);
        height: 100%;
        width: 100%;
        position: relative;
    }
    .jumbotron-container__middle img{
        width: 25%;
        position: absolute;
    }
    .jumbotron-container__middle .title{
        position: absolute;
        bottom: 290px;
        background-color: rgba(255, 255, 255, 0.8);
        padding: .3125rem .625rem;
        border-radius: .625rem;
    }
    .jumbotron-container__middle h1{
        background-image: linear-gradient(#bd34fe 30%, #41d1ff );
        -webkit-background-clip: text;
        -moz-background-clip: text;
        background-clip: text;
        color: transparent;
        text-align: center;
    }
    .jumbotron-container__right{
        width: 30%;
    }
    .jumbotron-container__left, .jumbotron-container__right{
        padding: 1.5625rem;
    }

    /*------------------
        CARD STYLE
    -------------------*/
    .card{
        background-color: #2f2f2f;
        padding: .9375rem 1.5625rem;
        border-radius: 1.25rem;
        margin-bottom: .625rem;
        min-height: 150px;
    }
    .card__icon span{
        display: inline-block;
        background-color: #242424;
        width: 2.5rem;
        height: 2.5rem;
        text-align: center;
        line-height: 2.5rem;
        border-radius: .625rem;
        font-size: 1.25rem;
    }
    .card__title h3{
        margin: .625rem 0;
    }
</style>