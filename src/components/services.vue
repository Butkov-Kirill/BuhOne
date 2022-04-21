<script>
import Card from './otherComponents/card-services.vue';

export default{
    components: {
        Card
    }
}
</script>

<template lang="pug">
.services
    p.p Наши услуги
    h1.name-page Мы специализируемся
    .cards
        .line-card
            Card(innerText='Бухгалтерское обслуживание', pathToPhoto='src/assets/images/picture.png')
            Card(innerText='Бухгалтерское обслуживание', pathToPhoto='src/assets/images/picture.png')
            Card(innerText='Бухгалтерское обслуживание', pathToPhoto='src/assets/images/picture.png')
        .line-card
            Card(innerText='Бухгалтерское обслуживание', pathToPhoto='src/assets/images/picture.png')
            Card(innerText='Бухгалтерское обслуживание', pathToPhoto='src/assets/images/picture.png')
            Card(innerText='Бухгалтерское обслуживание', pathToPhoto='src/assets/images/picture.png')
</template>

<style lang="scss">
.services{
    background: #EBEBEB;
    padding: 0 10% 0 10%;
    display: flex;
    flex-direction: column;
    .p{
        margin-top: 140px;
        font-family: 'Lato';
        font-style: normal;
        font-weight: 900;
        font-size: 24px;
        color: #BDBDBD;
    }
    .name-page{
        font-family: 'Merriweather';
        font-style: normal;
        font-weight: 900;
        font-size: 48px;
        color: #333333;
        margin-bottom: 100px;
    }
    .line-card{
        display: flex;
        padding-bottom: 30px;
    }
    .cards{
        margin: 0 auto;
        margin-bottom: 140px;
    }
}

@media (max-width: 800px){
    .services{
        .p{
            margin-top: 50px;
            font-size: 18px;
        }
        .name-page{
            font-size: 22px;
            margin-bottom: 50px;
        }
        .line-card{
            flex-direction: column;
            padding-bottom: 0;
        }
        .cards{
            margin: 0;
            margin-bottom: 50px;
        }
    }
}
</style>