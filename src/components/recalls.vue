<script>
import OptionBar from './otherComponents/scroll-buttons-bar.vue';
import Recall from './otherComponents/recall.vue';

export default {
    components: {
        OptionBar,
        Recall
    }
}
</script>

<template lang="pug">
.recalls
    p.name-page Отзывы
    h1.heading Ваши благодарности
    Recall
    OptionBar(color_point = "#005FA3", color_button = '#005FA3', id_bar='3')
</template>

<style lang="scss">
.recalls{
    padding-left: 10%;
    padding-right: 10%;
    padding-top: 140px;
    .name-page{
        font-family: 'Lato';
        font-style: normal;
        font-weight: 900;
        font-size: 24px;
        color: #BDBDBD;
    }
    .heading{
        font-family: 'Merriweather';
        font-style: normal;
        font-weight: 900;
        font-size: 48px;
        color: #333333;
        padding-bottom: 80px;
    }
}

@media (max-width: 800px){
    .recalls{
        padding-top: 50px;
        .name-page{
            font-size: 20px;
        }
        .heading{
            font-size: 22px;
            padding-bottom: 50px;
        }
    }
}
</style>