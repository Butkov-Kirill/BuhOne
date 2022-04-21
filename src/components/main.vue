<script>
import ScrollButtonsBar from './otherComponents/scroll-buttons-bar.vue';

export default{
    components: {
        ScrollButtonsBar
    },
    methods: {
        signal(){
            alert("Это тестовая версия сайта");
        }
    }
}
</script>

<template lang="pug">
.main
    h1 Бухгалтерские услуги <br> в Санкт-Петербурге
    button.button-main(@mousedown='signal()') Наша презентация
    ScrollButtonsBar(color_point="#fff", color_button="#fff", id_bar='1')
</template>

<style lang="scss">
.main{
    padding-left: 10%;
    padding-right: 10%;
    flex-direction: column;
    background: url('../assets/images/background-first-screen.png');
    background-size: cover;
    h1{
        margin-top: 170px;
        margin-bottom: 60px;
        color: #fff;
        font-family: 'Merriweather';
        font-style: normal;
        font-weight: 700;
        font-size: 48px;
        line-height: 66px;
    }
    .button-main{
        color: #fff;
        padding: 19px 70px 19px 70px;
        width: auto;
        background: #005FA3;
        border: none;
        font-family: 'Lato';
        font-style: normal;
        font-weight: 400;
        font-size: 18px;
        margin-bottom: 120px;

        &:hover{
            background: #00538f;
            transition: 0.2s;
        }
    }
}

@media (max-width: 800px) {
    .main{
        h1{
            margin-top: 50px;
            margin-bottom: 50px;
            font-size: 25px;
            line-height: 40px;
        }
        .button-main{
            padding: 19px 30px 19px 30px;
            font-size: 14px;
        }
    }
}
</style>